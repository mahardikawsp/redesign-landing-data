<script setup>
const topics = [
  "Administrasi Kependudukan dan Pencatatan Sipil",
  "Ekonomi",
  "Kearsipan",
  "Keberencanaan",
  "Kebudayaan",
  "Kelautan dan Perikanan",
  "Kemiskinan",
  "Sosial",
  "Kepegawaian, Pendidikan dan Pelatihan",
  "Kepemudaan dan Olah Raga",
  "Keuangan",
  "Kesatuan Bangsa dan Politik",
  "Ketentraman, Ketertiban Umum dan Perlindungan Masyarakat",
  "Komunikasi dan Informatika",
  "Koperasi, Usaha Kecil dan Menengah",
];

const selectedTopics = ref([]);
</script>

<template>
  <div
    class="modal fade"
    id="modalTopik"
    tabindex="-1"
    aria-labelledby="exampleModalLabel"
    aria-hidden="true"
  >
    <div
      class="modal-dialog modal-dialog-centered modal-dialog-scrollable modal-lg"
    >
      <div class="modal-content p-2">
        <div class="modal-header border-bottom-0 pb-1">
          <h1 class="modal-title fw-bold fs-5" id="exampleModalLabel">
            Personalisasi Konten
          </h1>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
          <p class="h-text-body-14 h-text-secondary">
            Pilih topik yang paling Anda minati untuk ditampilkan <br />
            sebagai tampilan default pada saat membuka website Satudata
            Banyuwangi.
          </p>
          <div class="d-flex flex-column flex-md-row align-items-md-center gap-3 justify-content-md-between my-5">
            <p class="h-text-heading-16">Pilih topik yang diminati</p>
            <div class="col-lg-5">
              <div class="input-group-lg position-relative">
                <label
                  for="exampleFormControlInput1"
                  class="sr-only d-none visually-hidden"
                  >Cari Topik</label
                >
                <input
                  type="text"
                  class="h-input-search h-input-search--sm form-control rounded"
                  id="exampleFormControlInput1"
                  placeholder="Cari Topik"
                />
              </div>
            </div>
          </div>
          <div class="row">
            <div class="col-md-6" v-for="(topic, index) in topics" :key="index">
              <div
                class="form-check mb-2"
                :class="{ 'form-check-active': selectedTopics.includes(topic) }"
              >
                <input
                  class="form-check-input"
                  type="checkbox"
                  :value="topic"
                  :id="'flexCheckChecked' + index"
                  v-model="selectedTopics"
                />
                <label
                  class="form-check-label h-text-body-14"
                  :for="'flexCheckChecked' + index"
                >
                  {{ topic }}
                </label>
              </div>
            </div>
          </div>
        </div>
        <div class="modal-footer justify-content-end  justify-content-md-between border-top-0 gap-1">
          <div class="d-flex align-items-center gap-3">
            <p class="h-text-body-16">3 topik dipilih</p>
            <button
              type="button"
              class="h-btn-outline--danger h-btn--icon"
            >
              <span>Reset</span>
              <i class="h-text-body-24 bi bi-x"></i>
            </button>
          </div>
          <div class="d-flex align-items-center gap-2">
            <button
              type="button"
              class="h-btn-outline--primary"
              data-bs-dismiss="modal"
            >
              Batalkan
            </button>
            <button type="button" class="h-btn--primary">
              Simpan
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
