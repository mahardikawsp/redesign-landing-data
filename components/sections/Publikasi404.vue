<template>
  <section class="h-section h-section__floating">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div
            class="d-flex flex-column flex-lg-row align-items-lg-center justify-content-between gap-4 mb-4"
          >
            <div class="d-flex flex-column gap-1">
              <p class="h-text-heading-16">
                Menampilkan hasil pencarian untuk <span>"Disabilitas"</span>
              </p>
              <p class="h-text-body-16">0 publikasi ditemukan</p>
            </div>
            <div class="d-block">
              <div class="input-group-lg">
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
      </div>
      <div
        class="row justify-content-center align-items-center text-center mt-5"
      >
        <div class="col-md-8 col-lg-6">
          <div
            class="d-flex flex-column align-items-center justify-content-center gap-4"
          >
            <img
              src="/images/section/publikasi-404.svg"
              class="img-fluid"
              height="305"
              width="415"
              loading="lazy"
              alt="logo"
            />
            <h2 class="h-text-heading-24">
              Publikasi yang Anda cari tidak ditemukan
            </h2>
            <p class="h-text-body-16">
              Cek kembali kata kunci dan filter yang dimasukkan. Atau Anda juga
              bisa melakukan request data yang diinginkan.
            </p>
            <button class="h-btn-outline--primary mb-4">Request Data</button>
          </div>
        </div>
      </div>
    </div>
  </section>
  <ModalsDownload />
</template>
