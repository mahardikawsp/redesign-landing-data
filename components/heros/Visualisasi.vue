<template>
  <header class="h-hero h-hero--visualisasi">
    <section
      class="h-hero__container d-flex flex-column justify-content-center"
    >
      <div class="container">
        <div class="row justify-content-center align-items-center text-md-center">
          <div class="col-md-10 col-lg-7">
            <div class="h-text-body-16 h-text-primary fw-semibold h-badge mb-4">
              Dashboard Data
            </div>
            <h1 class="h-text-heading-46 mb-3">Sajian visualisasi data Banyuwangi dalam satu saluran</h1>
            <p class="h-text-body-16 h-text-secondary">Jelajahi sajian informasi dengan visualisasi yang menarik, informatif, dan terintegrasi.</p>
            <div class="input-group-lg mt-5">
              <label
                for="exampleFormControlInput1"
                class="sr-only d-none visually-hidden"
                >Cari Data</label
              >
              <div class="row justify-content-center align-items-center">
                <div class="col-md-10">
                  <div class="input-group-lg position-relative">
                    <label
                      for="exampleFormControlInput1"
                      class="sr-only d-none visually-hidden"
                      >Cari Data</label
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
