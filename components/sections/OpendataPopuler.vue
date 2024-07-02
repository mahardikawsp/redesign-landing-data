<script setup>
const data = [
  {
    number: "1",
    title: "Jumlah Kelahiran Hidup",
    createdDate: "01-09-2022",
    views: 99,
    link: "/path-to-detail-1",
  },
  {
    number: "2",
    title: "Jumlah Kendaraan Sepeda Motor 500cc Melalui Penyeberangan Ketapang",
    createdDate: "01-09-2022",
    views: 99,
    link: "/path-to-detail-2",
  },
  {
    number: "3",
    title: "Jumlah Penerbangan Datang Melalui Bandara Blimbingsari",
    createdDate: "01-09-2022",
    views: 99,
    link: "/path-to-detail-3",
  },
  {
    number: "4",
    title: "Balita ditimbang (D/S)",
    createdDate: "01-09-2022",
    views: 99,
    link: "/path-to-detail-4",
  },
];
</script>

<template>
  <section class="h-section">
    <div class="container">
      <div class="row">
        <div class="col-md-5">
          <div class="container position-relative">
            <img src="/images/icon/line.svg" class="h-section-open-data--icon-line img-fluid" loading="lazy" alt="line">
            <div
              class="h-text-body-14 h-text-primary fw-semibold h-badge mb-3"
            >
              Data Terpopuler
            </div>
            <h2 class="h-text-heading-36 mb-3">
              Lihat pencarian data populer kami
            </h2>
            <p class="h-text-body-16">
              Telusuri indikator paling populer dan paling dicari pengguna di
              website kami, untuk memberikan Anda gambaran singkat tentang apa
              yang paling diminati.
            </p>
          </div>
        </div>
        <div class="col-md-7">
          <div class="container mt-5 mt-md-0">
            <div
              v-for="(item, index) in data"
              :key="index"
              class="h-card-number"
            >
              <div class="h-card-number__round">
                <span class="h-text-heading-24">{{ item.number }}</span>
              </div>
              <div class="d-flex flex-column gap-2">
                <h3 class="h-text-heading-24">{{ item.title }}</h3>
                <div
                  class="d-flex flex-column flex-md-row align-items-md-center gap-2 gap-md-5"
                >
                  <div class="d-flex align-items-center gap-2">
                    <i class="bi bi-calendar4 h-text-blue"></i>
                    <p class="h-text-secondary">Dibuat:</p>
                    <p class="h-text-secondary">{{ item.createdDate }}</p>
                  </div>
                  <div class="d-flex align-items-center gap-2">
                    <i class="bi bi-eye h-text-blue"></i>
                    <p class="h-text-secondary">Dilihat:</p>
                    <p class="h-text-secondary">{{ item.views }} user</p>
                  </div>
                </div>
                <NuxtLink
                  :to="item.link"
                  class="h-card-dotted__link d-flex align-content-center gap-2 fw-bold mt-2"
                >
                  <span>Lihat Detail</span>
                  <i class="h-text-blue bi bi-chevron-right"></i>
                </NuxtLink>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
