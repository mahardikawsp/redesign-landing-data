<script setup>
const years = ['2016', '2017', '2018', '2019', '2020', '2021', '2022'];
const dataList = ref([
  { id: 1, indicator: 'Jumlah Penerbangan Datang Melalui Bandara Blimbingsari', values: [955, 955, 955, 955, 955, '-', '-'] },
]);
</script>

<template>
  <div class="h-card-outline mt-5">
    <div class="d-flex flex-column flex-md-row justify-content-between gap-3 md:align-items-center mb-3">
      <h2 class="h-text-heading-18 text-start">Data Lainnya</h2>
      <div class="d-flex flex-column flex-md-row gap-2 md:gap-4">
        <div class="d-flex align-items-center gap-2">
          <div class="h-h-3 h-w-3 h-bg-warning rounded-1"></div>
          <p class="h-text-secondary">Sementara</p>
        </div>
        <div class="d-flex align-items-center gap-2">
          <div class="h-h-3 h-w-3 h-bg-danger rounded-1"></div>
          <p class="h-text-secondary">Sangat Sementara</p>
        </div>
      </div>
    </div>
    <div class="overflow-auto">
      <table class="table">
      <thead class="table-light rounded-4">
        <tr class="text-start rounded-2 bg-black">
          <th class="h-text-body-14 fw-bold" scope="col">Indikator</th>
          <th v-for="year in years" :key="year" class="h-text-body-14 fw-bold" scope="col">{{ year }}</th>
        </tr>
      </thead>
      <tbody>
        <tr class="text-start" v-for="data in dataList" :key="data.id">
          <th class="h-text-body-14" scope="row">{{ data.indicator }}</th>
          <td class="h-text-body-14" v-for="value in data.values" :key="value">{{ value }}</td>
        </tr>
      </tbody>
    </table>
    </div>
  </div>
</template>
