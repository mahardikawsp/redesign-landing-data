<script setup>
const organizations = ref([
  {
    name: "Badan Kepegawaian, Pendidikan dan Pelatihan",
    logo: "/images/card/org.png",
    logoHeight: 48,
    logoWidth: 42,
    email: "bkd@banyuwangikab.go.id",
    phone: "0812349502481",
    dataIndicators: 63,
  },
  {
    name: "Badan Kepegawaian, Pendidikan dan Pelatihan",
    logo: "/images/card/org.png",
    logoHeight: 48,
    logoWidth: 42,
    email: "bkd@banyuwangikab.go.id",
    phone: "0812349502481",
    dataIndicators: 63,
  },
  {
    name: "Badan Kepegawaian, Pendidikan dan Pelatihan",
    logo: "/images/card/org.png",
    logoHeight: 48,
    logoWidth: 42,
    email: "bkd@banyuwangikab.go.id",
    phone: "0812349502481",
    dataIndicators: 63,
  },
  {
    name: "Badan Kepegawaian, Pendidikan dan Pelatihan",
    logo: "/images/card/org.png",
    logoHeight: 48,
    logoWidth: 42,
    email: "bkd@banyuwangikab.go.id",
    phone: "0812349502481",
    dataIndicators: 63,
  },
  {
    name: "Badan Kepegawaian, Pendidikan dan Pelatihan",
    logo: "/images/card/org.png",
    logoHeight: 48,
    logoWidth: 42,
    email: "bkd@banyuwangikab.go.id",
    phone: "0812349502481",
    dataIndicators: 63,
  },
  {
    name: "Badan Kepegawaian, Pendidikan dan Pelatihan",
    logo: "/images/card/org.png",
    logoHeight: 48,
    logoWidth: 42,
    email: "bkd@banyuwangikab.go.id",
    phone: "0812349502481",
    dataIndicators: 63,
  },
]);
</script>

<template>
  <div class="row">
    <div
      v-for="(organization, index) in organizations"
      :key="index"
      class="col-md-6 col-lg-4"
    >
      <div class="h-card-shadow">
        <div class="d-flex align-items-center gap-3">
          <img
            :src="organization.logo"
            class="img-fluid"
            :height="organization.logoHeight"
            :width="organization.logoWidth"
            loading="lazy"
            :alt="organization.name"
          />
          <h3 class="h-text-heading-18">{{ organization.name }}</h3>
        </div>
        <div class="h-card-shadow__divider my-3"></div>
        <div class="d-flex flex-column gap-2">
          <div class="d-flex align-items-center gap-2">
            <i class="h-text-blue bi bi-envelope"></i>
            <a
              :href="'mailto:' + organization.email"
              class="h-text-body-16 h-text-secondary d-block"
              >{{ organization.email }}</a
            >
          </div>
          <div class="d-flex align-items-center gap-2">
            <i class="h-text-blue bi bi-telephone"></i>
            <a
              :href="'tel:' + organization.phone"
              class="h-text-body-16 h-text-secondary d-block"
              >{{ organization.phone }}</a
            >
          </div>
          <div class="d-flex align-items-center gap-2">
            <i class="h-text-blue bi bi-database"></i>
            <p class="h-text-body-16 h-text-secondary d-block">
              {{ organization.dataIndicators }} Indikator data
            </p>
          </div>
        </div>
        <div class="d-flex align-items-center justify-content-between mt-3">
          <a :href="'#'" class="h-card-shadow__link">Lihat Detail</a>
          <button class="h-card-shadow__button">
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
