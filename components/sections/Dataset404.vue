<template>
  <div class="d-flex flex-column flex-md-row justify-content-between gap-4">
    <div>
      <p class="h-text-heading-16">
        Menampilkan hasil pencarian untuk <b>"Natal"</b>
      </p>
      <p class="h-text-body-14">0 data ditemukan</p>
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
  <div class="row justify-content-center align-items-center text-center mt-5">
    <div class="col-md-8 col-lg-6">
      <div
        class="d-flex flex-column align-items-center justify-content-center gap-4"
      >
        <img
          src="/images/section/data-404.svg"
          class="img-fluid"
          height="305"
          width="415"
          loading="lazy"
          alt="logo"
        />
        <h2 class="h-text-heading-24">Data yang Anda cari tidak ditemukan</h2>
        <p class="h-text-body-16">
          Cek kembali kata kunci dan filter yang dimasukkan. Atau Anda juga bisa
          melakukan request data yang diinginkan.
        </p>
        <button class="h-btn-outline--primary mb-4">Request Data</button>
      </div>
    </div>
  </div>
</template>
