<template>
  <section class="h-section">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div
            class="d-flex flex-column flex-lg-row align-items-lg-center justify-content-between gap-2 mb-4"
          >
            <h2 class="h-text-heading-28">Daftar Organisasi</h2>
            <div class="col-xs-5">
              <div class="dropdown">
                <button
                  class="h-btn-outline--primary w-auto h-btn--icon dropdown-toggle"
                  type="button"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  <span>Urutkan Berdasarkan</span>
                  <i class="bi bi-chevron-down"></i>
                </button>
                <ul class="dropdown-menu">
                  <li>
                    <a class="dropdown-item h-text-body-14" href="#"
                      >Semua Organisasi</a
                    >
                  </li>
                  <li>
                    <a class="dropdown-item h-text-body-14" href="#"
                      >Intansi Pemkab Banyuwangi</a
                    >
                  </li>
                  <li>
                    <a class="dropdown-item h-text-body-14" href="#"
                      >Instansi Vertikal</a
                    >
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
        <CardsOrganization />
        <div class="d-flex justify-content-center align-items-center">
          <Pagination />
        </div>
      </div>
    </div>
  </section>
</template>
