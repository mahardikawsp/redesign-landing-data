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
    id="modalRequest"
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
            Request Data
          </h1>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
          <div class="col-md-8">
            <p class="h-text-body-16 h-text-secondary">
            Layanan untuk meminta data, dimana data tersebut tidak terbuka atau
            data bersifat pribadi yang tidak dipublikasikan.
          </p>
          </div>
          <div class="row mt-4">
            <div class="col-md-6">
              <div class="input-group-lg mb-3">
                <label
                  for="exampleFormControlInput1"
                  class="form-label h-text-body-14 fw-semibold"
                  >Nama Anda</label
                >
                <input
                  type="text"
                  class="form-control"
                  id="exampleFormControlInput1"
                  placeholder="Masukkan Nama Anda"
                />
              </div>
              <div class="input-group-lg mb-3">
                <label
                  for="exampleFormControlInput1"
                  class="form-label h-text-body-14 fw-semibold"
                  >Email</label
                >
                <input
                  type="email"
                  class="form-control"
                  id="exampleFormControlInput1"
                  placeholder="Masukkan Email Anda"
                />
              </div>
            </div>
            <div class="col-md-6">
              <div class="input-group-lg mb-3">
                <label
                  for="exampleFormControlInput1"
                  class="form-label h-text-body-14 fw-semibold"
                  >Instansi</label
                >
                <input
                  type="text"
                  class="form-control"
                  id="exampleFormControlInput1"
                  placeholder="Masukkan Nama Instansi"
                />
              </div>
              <div class="input-group-lg mb-3">
                <label
                  for="exampleFormControlInput1"
                  class="form-label h-text-body-14 fw-semibold"
                  >No. Handphone</label
                >
                <input
                  type="text"
                  class="form-control"
                  id="exampleFormControlInput1"
                  placeholder="Masukkan Nomor Handphone"
                />
              </div>
            </div>
          </div>
          <div class="mb-3">
            <label
              for="exampleFormControlTextarea1"
              class="form-label h-text-body-14 fw-semibold"
              >Data yang diperlukan</label
            >
            <textarea
              class="form-control"
              id="exampleFormControlTextarea1"
              placeholder="Masukkan pesan anda di sini"
              rows="5"
            ></textarea>
          </div>
          <div class="mb-3">
            <label for="formFile" class="form-label h-text-body-14 fw-semibold"
              >Upload file pendukung</label
            >
            <input class="form-control" type="file" id="formFile" />
          </div>
        </div>
        <div class="modal-footer justify-content-end border-top-0 gap-1">
          <div class="d-flex align-items-center gap-2">
            <button
              type="button"
              class="h-btn-outline--primary"
              data-bs-dismiss="modal"
            >
              Batalkan
            </button>
            <button type="button" class="h-btn--primary">
              Kirim
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
