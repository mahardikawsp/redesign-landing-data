<template>
  <div
    id="ExTopic"
    class="carousel slide container position-relative"
    data-bs-ride="carousel"
  >
    <div class="carousel-inner w-100">
      <div
        v-for="(item, index) in carouselItems"
        :key="index"
        class="justify-contents-center"
        :class="{ 'carousel-item': true, active: index === 0 }"
      >
        <div class="col-md-6 col-lg-3">
          <div class="h-card-shadow h-card-shadow--slider">
            <div>
              <div class="d-flex flex-column gap-3">
              <div class="d-flex align-items-center gap-2">
              <i
                :class="[
                  `h-icon-color--${item.color}`,
                  'h-text-heading-18',
                  item.icon,
                ]"
              ></i>
              <h3 class="h-text-heading-18">{{ item.name }}</h3>
            </div>
            <p class="h-text-secondary mt-5 mb-3">
              {{ item.description }}
            </p>
            </div>
            <div class="d-flex align-items-center justify-content-between mt-3">
              <a :href="item.detailLink" class="h-card-topic__link"
                >Lihat Detail</a
              >
              <button class="h-card-topic__button"></button>
            </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <button
      class="h-slider__navigation h-slider__navigation--left carousel-control-prev"
      type="button"
      data-bs-target="#ExTopic"
      data-bs-slide="prev"
    >
      <i class="bi bi-chevron-left"></i>
    </button>
    <button
      class="h-slider__navigation h-slider__navigation--right carousel-control-next"
      type="button"
      data-bs-target="#ExTopic"
      data-bs-slide="next"
    >
      <i class="bi bi-chevron-right"></i>
    </button>
  </div>
  <div class="col-11">
    <button class="h-btn-outline--primary d-block d-md-none">Lihat topik lainnya</button>
  </div>
</template>

<script setup>
const carouselItems = ref([
  {
    id: 1,
    name: "Pendidikan",
    icon: "bi bi-mortarboard",
    color: "purple",
    description:
      "Pengetahuan generasi ke generasi berikutnya melalui pelatihan, atau penelitian.",
    detailLink: "#",
  },
  {
    id: 2,
    name: "Kesehatan",
    icon: "bi bi-heart-pulse",
    color: "red",
    description:
      "Kesejahteraan fisik, mental, sosial dan tidak adanya penyakit atau kelemahan.",
    detailLink: "#",
  },
  {
    id: 3,
    name: "Sosial",
    icon: "bi bi-person-check",
    color: "green",
    description:
      "Hidup secara aktif serta kolektif dalam populasi yang saling berinteraksi.",
    detailLink: "#",
  },
  {
    id: 4,
    name: "Tenaga Kerja",
    icon: "bi bi-briefcase",
    color: "brown",
    description:
      "Melakukan pekerjaan guna menghasilkan barang, produk, dan jasa.",
    detailLink: "#",
  },
  {
    id: 5,
    name: "Pariwisata",
    icon: "bi bi-luggage",
    color: "ivory",
    description:
      "Rekreasi atau liburan dan juga persiapan lainnya yang dilakukan untuk aktivitas ini.",
    detailLink: "#",
  },
  {
    id: 6,
    name: "Ekonomi",
    icon: "bi bi-bar-chart-line",
    color: "pink",
    description: "Mengelola sumber daya yang terbatas dan menyalurkannya.",
    detailLink: "#",
  },
  {
    id: 7,
    name: "Kemiskinan",
    icon: "bi bi-graph-down-arrow",
    color: "green",
    description:
      "Keadaan diri seseorang saat tidak mampu untuk memenuhi kebutuhan dasar.",
    detailLink: "#",
  },
  {
    id: 8,
    name: "Pertanian",
    icon: "bi bi-tree",
    color: "yellow",
    description:
      "Pemanfaatan sumber daya alam hayati dalam kelola lingkungan hidup.",
    detailLink: "#",
  },
]);

const cardCarousel = () => {
  const minPerSlide = 4;

  document.querySelectorAll(".carousel .carousel-item").forEach((element) => {
    let next = element.nextElementSibling;

    if (!next) {
      next = element.parentElement.firstElementChild;
    }

    element.appendChild(next.firstElementChild.cloneNode(true));

    for (let i = 0; i < minPerSlide; i++) {
      next = next.nextElementSibling;

      if (!next) {
        next = element.parentElement.firstElementChild;
      }

      element.appendChild(next.firstElementChild.cloneNode(true));
    }
  });
};

onMounted(() => {
  cardCarousel();
});
</script>

<style lang="scss" scoped>
@media (max-width: 768px) {
  .carousel-inner {
    .carousel-item {
      > div {
        display: none;
        &:first-child {
          display: block;
        }
      }
    }
  }
}
.carousel-inner {
  .carousel-item.active {
    display: flex;
  }
  .carousel-item-start {
    display: flex;
  }
  .carousel-item-next {
    display: flex;
  }
  .carousel-item-prev {
    display: flex;
  }
}
@media (min-width: 768px) {
  .carousel-inner {
    .carousel-item-right.active {
      transform: translateX(25%) !important;
    }
    .carousel-item-next {
      transform: translateX(25%) !important;
    }
    .carousel-item-left.active {
      transform: translateX(-25%) !important;
    }
    .carousel-item-prev {
      transform: translateX(-25%) !important;
    }
  }
  .carousel-item-next {
    &:not(.carousel-item-start) {
      transform: translateX(25%) !important;
    }
  }
  .carousel-item-prev {
    &:not(.carousel-item-end) {
      transform: translateX(-25%) !important;
      transform: translateX(-25%) !important;
      transform: translateX(-25%) !important;
    }
  }
  .active.carousel-item-start {
    transform: translateX(-25%) !important;
  }
  .carousel-item-next.carousel-item-start {
    transform: translateX(0) !important;
  }
  .active.carousel-item-end {
    transform: translateX(0) !important;
  }
  .carousel-control-prev {
    color: var(--dark) !important;
  }
  .carousel-control-next {
    color: var(--dark) !important;
  }
}
</style>
