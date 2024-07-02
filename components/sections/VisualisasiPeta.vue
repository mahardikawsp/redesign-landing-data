<script setup>
const linkData = ref([
  {
    url: "#",
    text: "Kepadatan Penduduk Berdasarkan Daerah di Banyuwangi",
  },
  {
    url: "#",
    text: "Angka Harapan Hidup Berdasarkan Daerah di Banyuwangi",
  },
  {
    url: "#",
    text: "Indeks Kesehatan Berdasarkan Daerah di Banyuwangi",
  },
  {
    url: "#",
    text: "Jumlah Rumah Sakit (RS) Berdasarkan Daerah di Banyuwangi",
  },
  {
    url: "#",
    text: "Jumlah Dokter Umum Berdasarkan Daerah di Banyuwangi",
  },
  {
    url: "#",
    text: "Pendapatan Rata-Rata Penduduk Berdasarkan Daerah di Banyuwangi",
  },
  {
    url: "#",
    text: "Persentase Pendidikan Tinggi Berdasarkan Daerah di Banyuwangi",
  },
  {
    url: "#",
    text: "Jumlah Lapangan Kerja Berdasarkan Daerah di Banyuwangi",
  },
  {
    url: "#",
    text: "Persentase Penggunaan Energi Terbarukan Berdasarkan Daerah di Banyuwangi",
  },
  {
    url: "#",
    text: "Indeks Kriminalitas Berdasarkan Daerah di Banyuwangi",
  },
]);
</script>

<template>
  <section class="h-section">
    <div class="h-card">
      <div class="row gap-5 gap-md-0">
        <div class="col-md-4">
          <div class="h-card-filter">
            <div class="h-card-filter__wrapper">
              <p class="h-text-heading-18">Visualisasi Peta</p>
              <div class="my-4">
                <div class="input-group-lg position-relative">
                  <label
                    for="exampleFormControlInput1"
                    class="sr-only d-none visually-hidden"
                    >Cari Daerah</label
                  >
                  <input
                    type="text"
                    class="h-input-search h-input-search--sm form-control rounded"
                    id="exampleFormControlInput1"
                    placeholder="Cari daerah"
                  />
                </div>
              </div>
              <div class="h-card-filter__overflow">
                <div
                  v-for="(link, index) in linkData"
                  :key="index"
                  class="border-bottom p-2"
                >
                  <a :href="link.url" class="h-text-body-16 h-text-primary fw-semibold">{{
                    link.text
                  }}</a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-8">
          <div class="responsive-map">
            <iframe
              src="https://maps.google.com/maps?q=banyuwangi&t=&z=10&ie=UTF8&iwloc=&output=embed"
              width="600"
              height="450"
              frameborder="0"
              style="border: 0"
              allowfullscreen
            ></iframe>
          </div>
        </div>
      </div>
      <div class="h-card--soft mt-4">
        <div class="d-flex align-items-center gap-2">
          <i class="bi bi-info-circle"></i>
          <p class="h-text-heading-14">
            Sumber Data:
            <span class="h-text-body-14"
              >Dataset Jumlah Dokter Gigi Berdasarkan Kabupaten/Kota di
              Banyuwangi - Tahun 2022</span
            >
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.responsive-map {
  overflow: hidden;
  padding-bottom: 56.25%;
  position: relative;
  height: 0;

  iframe {
    border-radius: 12px;
    left: 0;
    top: 0;
    height: 100%;
    width: 100%;
    position: absolute;
  }
}
</style>
