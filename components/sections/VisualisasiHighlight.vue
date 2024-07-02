<script setup>
const carouselItems = ref([
  {
    iconClass: "h-card__icon--navy bi bi-people",
    title: "Kependudukan",
    date: "Data tahun 2022",
    items: [
      { label: "Jumlah Penduduk", value: "48.220.094 Jiwa" },
      { label: "Kepadatan Penduduk", value: "1.297,47 Jiwa/km2" },
      { label: "Luas Wilayah", value: "37.164,6 km2" },
    ],
  },
  {
    iconClass: "h-card__icon--maroon bi bi-heart-pulse",
    title: "Kesehatan",
    date: "Data tahun 2022",
    items: [
      { label: "Jumlah Penduduk", value: "48.220.094 Jiwa" },
      { label: "Kepadatan Penduduk", value: "1.297,47 Jiwa/km2" },
      { label: "Luas Wilayah", value: "37.164,6 km2" },
    ],
  },
  {
    iconClass: "h-card__icon--green bi bi-person-check",
    title: "Sosial",
    date: "Data tahun 2022",
    items: [
      { label: "Jumlah Penduduk", value: "48.220.094 Jiwa" },
      { label: "Kepadatan Penduduk", value: "1.297,47 Jiwa/km2" },
      { label: "Luas Wilayah", value: "37.164,6 km2" },
    ],
  },
  {
    iconClass: "h-card__icon--brown bi bi-briefcase",
    title: "Tenaga Kerja",
    date: "Data tahun 2022",
    items: [
      { label: "Jumlah Penduduk", value: "48.220.094 Jiwa" },
      { label: "Kepadatan Penduduk", value: "1.297,47 Jiwa/km2" },
      { label: "Luas Wilayah", value: "37.164,6 km2" },
    ],
  },
]);

const highlightCarousel = () => {
  const minPerSlide = 2;

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
  highlightCarousel();
});
</script>

<template>
  <section class="h-section position-relative">
    <img src="/images/icon/curve.svg" class="h-section-topik--icon img-fluid d-none d-md-block" loading="lazy" alt="line">
    <div class="container">
      <div class="row">
        <div class="d-flex flex-column flex-md-row justify-content-between align-items-md-center gap-3">
          <h2 class="h-text-heading-24">Highlight data</h2>
          <div class="col-md-5">
            <p class="h-text-body-16">
              Website Satudata Banyuwangi berfungsi sebagai sumber data dari
              berbagai badan atau organisasi daerah yang ada di Banyuwangi. Anda
              bisa mencari sumber Open Data maupun Satu Data.
            </p>
          </div>
        </div>
        <div
          id="ExHighlight"
          class="carousel slide container position-relative mt-5"
          data-bs-ride="carousel"
        >
          <div class="carousel-inner w-100">
            <div
              v-for="(item, index) in carouselItems"
              :key="index"
              class="justify-contents-center"
              :class="{ 'carousel-item': true, active: index === 0 }"
            >
              <div class="col-12 col-lg-6">
                <div class="h-card h-card--slider">
                  <div
                    class="d-flex flex-column flex-md-row justify-content-between align-items-md-center mb-4"
                  >
                    <div class="d-flex align-items-center gap-2">
                      <i :class="item.iconClass"></i>
                      <p class="h-text-heading-18">{{ item.title }}</p>
                    </div>
                    <p class="h-text-body-14 h-text-secondary">
                      {{ item.date }}
                    </p>
                  </div>
                  <div
                    class="d-flex flex-column flex-md-row justify-content-between gap-4 align-items-md-center"
                  >
                    <div
                      v-for="(item, itemIndex) in item.items"
                      :key="itemIndex"
                      class="d-flex flex-column align-items-md-center gap-1"
                    >
                      <p class="h-text-14">{{ item.label }}</p>
                      <p class="h-text-heading-16">{{ item.value }}</p>
                    </div>
                    <div
                      v-if="itemIndex < item.items.length - 1"
                      class="h-card__border--right"
                    ></div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <button
            class="h-slider__navigation h-slider__navigation--left-1 carousel-control-prev"
            type="button"
            data-bs-target="#ExHighlight"
            data-bs-slide="prev"
          >
            <i class="bi bi-chevron-left"></i>
          </button>
          <button
            class="h-slider__navigation h-slider__navigation--right-1 carousel-control-next"
            type="button"
            data-bs-target="#ExHighlight"
            data-bs-slide="next"
          >
            <i class="bi bi-chevron-right"></i>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

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
