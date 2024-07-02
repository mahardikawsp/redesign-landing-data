<script setup>
const publications = ref([
  {
    image: "/images/card/thumb-3.png",
    title: "Evaluasi Program Pemerintah Desa Tahun 2021",
    link: "/",
    download: "#downloadModal",
  },
  {
    image: "/images/card/thumb-1.png",
    title: "Implementasi Sistem Informasi Kepegawaian di Pemerintah Kota XYZ",
    link: "/",
    download: "#downloadModal",
  },
  {
    image: "/images/card/thumb-2.png",
    title: "Strategi Peningkatan Kualitas Pelayanan Publik di Kabupaten ABC",
    link: "/",
    download: "#downloadModal",
  },
  {
    image: "/images/card/thumb-4.png",
    title:
      "Analisis Kepuasan Masyarakat Terhadap Layanan Dinas Pendidikan Kabupaten XYZ",
    link: "/",
    download: "#downloadModal",
  },
  {
    image: "/images/card/thumb-2.png",
    title: "Strategi Peningkatan Kualitas Pelayanan Publik di Kabupaten ABC",
    link: "/",
    download: "#downloadModal",
  },
  {
    image: "/images/card/thumb-3.png",
    title:
      "Optimalisasi Penggunaan Teknologi Informasi di Pemerintah Provinsi ABC",
    link: "/",
    download: "#downloadModal",
  },
  {
    image: "/images/card/thumb-2.png",
    title: "Strategi Peningkatan Kualitas Pelayanan Publik di Kabupaten ABC",
    link: "/",
    download: "#downloadModal",
  },
  {
    image: "/images/card/thumb-4.png",
    title:
      "Analisis Kepuasan Masyarakat Terhadap Layanan Dinas Pendidikan Kabupaten XYZ",
    link: "/",
    download: "#downloadModal",
  },
]);
</script>

<template>
  <div v-for="(publication, i) in publications" :key="i" class="col-md-6 col-lg-3">
    <div class="h-card-thumb">
      <img
        :src="publication.image"
        class="h-card-thumb__image img-fluid"
        height="48"
        width="42"
        loading="lazy"
        alt="card"
      />
      <div class="p-4">
        <div class="col-md-11">
          <p class="h-card-thumb__title h-text-heading-16">
            {{ publication.title }}
          </p>
        </div>
        <div
          class="d-flex align-items-center justify-content-between gap-2 mt-4"
        >
          <a
            :href="publication.link"
            class="h-card-thumb__button d-flex justify-content-center align-items-center"
            >Lihat Detail</a
          >
          <button
            class="h-card-thumb__button-icon d-flex justify-content-center align-items-center"
            data-bs-toggle="modal"
            :data-bs-target="publication.download"
          >
            <i class="h-text-blue fw-bold bi bi-download"></i>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
