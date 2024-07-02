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
  {
    "id": 5,
    "name": "Pariwisata",
    "icon": "bi bi-luggage",
    "color": "ivory",
    "description": "Rekreasi atau liburan dan juga persiapan lainnya yang dilakukan untuk aktivitas ini.",
    "detailLink": "#"
  },
  {
    "id": 6,
    "name": "Ekonomi",
    "icon": "bi bi-bar-chart-line",
    "color": "pink",
    "description": "Mengelola sumber daya yang terbatas dan menyalurkannya.",
    "detailLink": "#"
  },
  {
    "id": 7,
    "name": "Kemiskinan",
    "icon": "bi bi-graph-down-arrow",
    "color": "green",
    "description": "Keadaan diri seseorang saat tidak mampu untuk memenuhi kebutuhan dasar.",
    "detailLink": "#"
  },
  {
    "id": 8,
    "name": "Pertanian",
    "icon": "bi bi-tree",
    "color": "yellow",
    "description": "Pemanfaatan sumber daya alam hayati dalam kelola lingkungan hidup.",
    "detailLink": "#"
  }
]
);
</script>

<template>
  <section class="h-section h-bg-warning">
    <div class="container position-relative">
      <img src="/images/icon/rectangle-orange.svg" class="h-section-open-data--icon-orange d-none d-md-block img-fluid" loading="lazy" alt="wafe">
      <img src="/images/icon/rectangle-blue.svg" class="h-section-open-data--icon-blue d-none d-md-block img-fluid" loading="lazy" alt="wafe">
      <div class="row justify-content-center mb-5">
        <div class="col-md-8 text-md-center">
          <div class="h-text-body-14 h-text-primary fw-semibold h-badge h-badge-dark bg-transparent mb-3">
            Topik Favorit
          </div>
          <h2 class="h-text-heading-36 mb-2">
            Telusuri topik yang paling diminati
          </h2>
          <p class="h-text-body-16 h-text-secondary">
            Urusan umum yang paling banyak sering dicari oleh pengguna.
          </p>
        </div>
      </div>
      <div class="row pt-5">
        <div v-for="topic in topics" :key="topic.id" class="col-md-3">
          <div class="h-card-topic">
            <div class="d-flex align-items-center gap-2">
              <i :class="[`h-icon-color--${topic.color}`, 'h-text-heading-18', topic.icon]"></i>
              <h3 class="h-text-heading-18">{{ topic.name }}</h3>
            </div>
            <p class="h-text-secondary mt-5 mb-3">
              {{ topic.description }}
            </p>
            <div class="d-flex align-items-center justify-content-between mt-3">
              <a :href="topic.detailLink" class="h-card-topic__link">Lihat Detail</a>
              <button class="h-card-topic__button"></button>
            </div>
          </div>
        </div>
      </div>
      <img src="/images/icon/wafe-blue.svg" class="h-section-open-data--icon-right d-none d-md-block img-fluid" loading="lazy" alt="wafe">
    </div>
  </section>
</template>
