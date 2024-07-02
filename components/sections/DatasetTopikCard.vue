<script setup>
const topics = ref([
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
]);
</script>

<template>
  <div class="row pt-5 mb-5">
    <div v-for="topic in topics" :key="topic.id" class="col-md-6 col-lg-3">
      <div class="h-card-shadow mb-3 mb-lg-0">
        <div class="d-flex align-items-center gap-2">
          <i :class="[`h-icon-color--${topic.color}`, 'h-text-heading-18', topic.icon]"></i>
          <h3 class="h-text-heading-18">{{ topic.name }}</h3>
        </div>
        <p class="h-text-secondary mt-5 mb-3">
          {{ topic.description }}
        </p>
        <div class="d-flex align-items-center justify-content-between mt-3">
          <a :href="topic.detailLink" class="h-card-topic__link"
            >Lihat Detail</a
          >
          <button class="h-card-topic__button"></button>
        </div>
      </div>
    </div>
  </div>
</template>
