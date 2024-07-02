<script setup>
const cardData = ref(
  Array.from({ length: 10 }, (_, index) => ({
    title: `Jumlah Kerjasama Pemerintah Dan Badan Usaha (KPBU) ${index + 1}`,
    tags: [
      { icon: "bi-building", label: "Sekertariat Daerah" },
      { icon: "bi-file-earmark-text", label: "Sekertariatan" },
    ],
  }))
);
</script>

<template>
  <section class="h-section">
    <div class="row">
      <div class="col-md-4 col-lg-3">
        <div class="h-card-filter">
          <div class="h-card-filter__wrapper">Pilih filter</div>
          <div class="h-card-filter__border"></div>
          <div class="h-card-filter__wrapper">
            <p class="h-text-heading-14 mb-2">Organisasi Perangkat Daerah</p>
            <a href="#" class="h-card-filter__link h-text-heading-14"
              >Pilih semua</a
            >
            <div class="mt-4">
              <input type="checkbox" class="h-readmore__state" id="readmore" />
              <div class="h-readmore__wrap">
                <div class="form-check mb-2">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckDefault"
                    checked
                  />
                  <label
                    class="form-check-label h-text-body-14"
                    for="flexCheckDefault"
                  >
                    Badan Penanggulangan Bencana Daerah
                  </label>
                </div>
                <div class="form-check mb-2">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckChecked"
                  />
                  <label
                    class="form-check-label h-text-body-14"
                    for="flexCheckChecked"
                  >
                    Badan Pendapatan Daerah
                  </label>
                </div>
                <div class="form-check mb-2 h-readmore__target">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckDefault"
                  />
                  <label
                    class="form-check-label h-text-body-14"
                    for="flexCheckDefault"
                  >
                    Badan Kepegawaian, Pendidikan dan Pelatihan
                  </label>
                </div>
                <div class="form-check mb-2 h-readmore__target">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckChecked"
                    checked
                  />
                  <label
                    class="form-check-label h-text-body-14"
                    for="flexCheckChecked"
                  >
                    Badan Kesatuan Bangsa dan Politik
                  </label>
                </div>
              </div>
              <label
                for="readmore"
                class="h-readmore__trigger h-text-heading-14"
              ></label>
            </div>
          </div>
          <div class="h-card-filter__border"></div>
          <div class="h-card-filter__wrapper">
            <p class="h-text-heading-14 mb-2">Pilih Topik Urusan</p>
            <a href="#" class="h-card-filter__link h-text-heading-14"
              >Pilih semua</a
            >
            <div class="mt-4">
              <input type="checkbox" class="h-readmore__state" id="readmore2" />

              <div class="h-readmore__wrap">
                <div class="form-check mb-2">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckDefault"
                    checked
                  />
                  <label
                    class="form-check-label h-text-body-14"
                    for="flexCheckDefault"
                  >
                  Administrasi Kependudukan dan Pencatatan Sipil
                  </label>
                </div>
                <div class="form-check mb-2">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckChecked"
                  />
                  <label
                    class="form-check-label h-text-body-14"
                    for="flexCheckChecked"
                  >
                  Ekonomi
                  </label>
                </div>
                <div class="form-check mb-2 h-readmore__target">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckDefault"
                  />
                  <label
                    class="form-check-label h-text-body-14"
                    for="flexCheckDefault"
                  >
                    Kearsipan
                  </label>
                </div>
                <div class="form-check mb-2 h-readmore__target">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckChecked"
                  />
                  <label
                    class="form-check-label h-text-body-14"
                    for="flexCheckChecked"
                  >
                  Kebencanaan
                  </label>
                </div>
              </div>
              <label
                for="readmore2"
                class="h-readmore__trigger h-text-heading-14"
              ></label>
            </div>
          </div>
        </div>
        <div class="h-card-shadow h-card-shadow--soft mt-4">
          <div class="d-flex flex-column gap-3">
            <i class="bi bi-file-earmark-arrow-up-fill h-text-heading-36 h-text-blue"></i>
            <p class="h-text-heading-16">Perlu data lainnya?</p>
            <p class="h-text-body-14 mb-3">Anda bisa request data lain yang sifatnya tidak terbuka.</p>
            <button class="h-btn--primary" data-bs-toggle="modal" data-bs-target="#modalRequest">Request Data</button>
          </div>
        </div>
      </div>
      <div class="col-md-8 col-lg-9">
        <div class="d-flex justify-content-between gap-4">
          <div>
            <p class="h-text-heading-16">Daftar data</p>
            <p class="h-text-body-14">463 data yang tersedia</p>
          </div>
          <div class="col-xs-5">
            <div class="dropdown">
            <button
              class="h-btn-outline--primary w-auto h-btn--icon dropdown-toggle"
              type="button"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              <span>Urutkan dari</span>
              <i class="bi bi-chevron-down"></i>
            </button>
            <ul class="dropdown-menu">
              <li>
                <a class="dropdown-item h-text-body-14" href="#">Terbaru</a>
              </li>
              <li>
                <a class="dropdown-item h-text-body-14" href="#">Abjad</a>
              </li>
              <li>
                <a class="dropdown-item h-text-body-14" href="#">Tanggal</a>
              </li>
              <li>
                <a class="dropdown-item h-text-body-14" href="#">Terpopuler</a>
              </li>
            </ul>
          </div>
          </div>
        </div>
        <div class="d-flex flex-column gap-4 mt-4">
          <div
            v-for="(item, index) in cardData"
            :key="index"
            class="h-card-outline"
          >
            <div
              class="d-flex flex-column flex-lg-row justify-content-between align-items-center gap-4"
            >
              <div class="d-flex flex-column flex-md-row align-items-md-center gap-4">
                <div>
                  <div class="h-card__icon">
                    <div class="h-card__icon-inner"></div>
                  </div>
                </div>
                <div>
                  <p class="h-text-heading-16 mb-3">{{ item.title }}</p>
                  <div class="d-flex gap-2">
                    <div
                      v-for="(tag, tagIndex) in item.tags"
                      :key="tagIndex"
                      class="d-flex align-items-center rounded-2 gap-2 border h-w-max px-2 py-1"
                    >
                      <i class="bi" :class="tag.icon"></i>
                      <p class="h-text-body-14">{{ tag.label }}</p>
                    </div>
                  </div>
                </div>
              </div>
              <a href="/dataset-detail" class="h-btn-outline--primary px-5 px-md-3">
                Lihat Detail
              </a>
            </div>
          </div>
        </div>
        <Pagination />
        <div class="mt-5"> <!-- If data not found please remove this class -->
          <SectionsDataset404 />
        </div>
      </div>
    </div>
  </section>
  <ModalsRequestData />
</template>
