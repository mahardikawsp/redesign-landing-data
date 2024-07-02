<script setup>
const cardData = ref([
  { icon: 'bi bi-database', title: 'Total Data', value: '1461', link: '#' },
  { icon: 'bi bi-folder-check', title: 'Total Urusan', value: '1461', link: '#' },
  { icon: 'bi bi-people', title: 'Total Organisasi', value: '141', link: '#' },
  { icon: 'bi bi-file-earmark-text', title: 'Total Publikasi', value: '11', link: '#' },
]);
</script>

<template>
  <section class="h-section">
    <div class="container h-card-fly">
      <div class="row justify-content-center h-card-fly-wrapper">
        <div class="col-md-12">
          <div class="row pt-5">
            <div
              v-for="(card, index) in cardData"
              :key="index"
              class="col-md-6 col-xl-3"
            >
              <div class="h-card-dotted h-bg-neutral-50">
                <div class="d-flex align-items-center gap-2 p-3">
                  <i
                    class="h-text-blue h-text-body-24"
                    :class="card.icon"
                  ></i>
                  <p class="h-text-heading-18">{{ card.title }}</p>
                </div>
                <div class="h-card-dotted__divider"></div>
                <div class="p-4">
                  <h3 class="h-text-heading-36 mb-4">{{ card.value }}</h3>
                  <router-link
                    :to="card.link"
                    class="h-card-dotted__link d-flex align-content-center gap-2 fw-bold"
                  >
                    <span>Lihat Detail</span>
                    <i class="h-text-blue bi bi-chevron-right"></i>
                  </router-link>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
