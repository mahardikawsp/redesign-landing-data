<script setup>
const data = [
  { label: "Kode SDSN", value: "66542" },
  { label: "Nomor Indikator", value: "66542" },
  { label: "Konsep", value: "66542" },
  { label: "Definisi", value: "66542" },
  { label: "Klasifikasi", value: "66542" },
  { label: "Ukuran", value: "66542" },
  { label: "Satuan", value: "66542" },
  { label: "Sumber Referensi", value: "66542" },
];
</script>

<template>
  <div class="row justify-content-between text-start">
    <div v-for="(item, index) in data" :key="index" class="col-6 col-md-3 mb-4">
      <div class="d-flex flex-column gap-1">
        <p class="h-text-body-16 h-text-secondary">{{ item.label }}</p>
        <p class="h-text-heading-18 h-text-primary">{{ item.value }}</p>
      </div>
    </div>
  </div>
</template>
