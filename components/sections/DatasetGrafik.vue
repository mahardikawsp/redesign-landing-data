<script setup>
const chartBar = ref({
  xAxis: {
    data: ["2016", "2017", "2018", "2019", "2020", "2021", "2022"],
  },
  yAxis: {
    type: "value",
  },
  series: [
    {
      type: "bar",
      data: [0, 600, 1200, 1800, 2400, 3000],
    },
  ],
  title: {
    text: "",
    x: "center",
    textStyle: {
      fontSize: 24,
    },
  },
  color: ["#3062e0"],
});
</script>

<template>
  <div class="h-card-outline mt-5">
    <div class="d-flex flex-column flex-md-row justify-content-between gap-3 text-start">
      <h2 class="h-text-heading-18">Grafik jumlah penerbangan datang</h2>
      <div class="col-xs-5">
        <div class="dropdown">
        <button class="h-btn-outline--primary w-auto h-btn--icon dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
          <span>Download</span>
          <i class="bi bi-chevron-down"></i>
        </button>
        <ul class="dropdown-menu">
          <li><a class="dropdown-item h-text-body-14" href="#">Download sebagai SVG</a></li>
          <li><a class="dropdown-item h-text-body-14" href="#">Download sebagai PNG</a></li>
          <li><a class="dropdown-item h-text-body-14" href="#">Download sebagai CSV</a></li>
        </ul>
      </div>
      </div>
    </div>
    <client-only>
      <EChart class="h-h-screen" :option="chartBar" />
    </client-only>
  </div>
</template>
