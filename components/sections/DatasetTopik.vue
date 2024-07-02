<template>
  <section class="h-section h-bg-gray-soft">
    <div class="container position-relative">
      <img src="/images/icon/three-stick.svg" class="h-section-dataset--icon-left img-fluid" loading="lazy" alt="stick">
      <img src="/images/icon/double-line.svg" class="h-section-dataset--icon-right img-fluid" loading="lazy" alt="line">
      <div class="d-flex flex-column flex-md-row align-items-center gap-4 justify-content-between">
        <h3 class="h-text-heading-36">Topik yang mungkin anda suka</h3>
        <button class="h-btn-outline--primary px-5 px-md-3">Lihat Semua</button>
      </div>
      <SectionsDatasetTopikCard />
    </div>
  </section>
</template>
