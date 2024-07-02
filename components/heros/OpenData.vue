<template>
  <header class="h-hero h-hero--open-data">
    <section
      class="h-hero__container d-flex flex-column justify-content-center"
    >
      <div class="container">
        <div class="row justify-content-center align-items-center text-md-center">
          <div class="col-md-6">
            <div class="h-text-body-16 h-text-primary fw-semibold h-badge mb-4">
              Open Data
            </div>
            <h1 class="h-text-heading-46 mb-3">Cari data Banyuwangi di sini</h1>
            <div class="input-group-lg mt-5">
              <label
                for="exampleFormControlInput1"
                class="sr-only d-none visually-hidden"
                >Cari Organisasi</label
              >
              <div class="row justify-content-center align-items-center">
                <div class="col-lg-10">
                  <div class="input-group-lg position-relative">
                    <label
                      for="exampleFormControlInput1"
                      class="sr-only d-none visually-hidden"
                      >Cari Organisasi</label
                    >
                    <input
                      type="text"
                      class="h-input-search form-control"
                      id="exampleFormControlInput1"
                      placeholder="Cari data disini"
                    />
                    <button
                      class="h-input-search__button h-btn--primary"
                    >
                      Cari Data
                    </button>
                  </div>
                </div>
              </div>
              <p class="mt-4 h-text-secondary">
                Topik pencarian populer:
                <span class="fw-semibold"><u>pendidikan, </u></span
                ><span class="fw-semibold"><u>tenaga kerja, </u></span
                ><span class="fw-semibold"><u>pariwisata</u></span>
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </header>
</template>
