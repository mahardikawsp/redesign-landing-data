<template>
  <section class="h-section h-section__floating">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div
            class="d-flex flex-column flex-lg-row align-items-lg-center justify-content-between gap-2 mt-5 mt-md-0 mb-5"
          >
            <h2 class="h-text-heading-28">Lihat Semua Publikasi</h2>
            <div class="col-md-3">
              <div class="input-group">
                <label
                  for="exampleFormControlInput1"
                  class="sr-only d-none visually-hidden"
                  >Cari publikasi</label
                >
                <input
                  type="text"
                  class="h-input-search h-input-search--md rounded form-control"
                  id="exampleFormControlInput1"
                  placeholder="Cari publikasi"
                />
              </div>
            </div>
          </div>
        </div>
        <CardsPublikasi />
      </div>
      <div
        class="row justify-content-center align-items-center text-center mt-4"
      >
        <div class="col-12">
          <button class="h-btn-outline--primary">Lihat Publikasi Lainya</button>
        </div>
      </div>
    </div>
  </section>
  <ModalsDownload />
</template>
