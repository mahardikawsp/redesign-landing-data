<script setup>
const menuItems = [
  { label: "Beranda", link: "/" },
  { label: "Dataset", link: "/dataset" },
  { label: "Visualisasi", link: "/visualisasi" },
  { label: "Organisasi", link: "/organisasi" },
  { label: "Publikasi", link: "/publikasi" },
  { label: "Topik", link: "/topik" },
  { label: "Tentang", link: "/tentang-kami"},
  { label: "FAQ", link: "/faq" },
];

const socialMediaLinks = [
  { iconClass: "bi bi-facebook", link: "#" },
  { iconClass: "bi bi-twitter", link: "#" },
  { iconClass: "bi bi-instagram", link: "#" },
  { iconClass: "bi bi-youtube", link: "#" },
];
</script>

<template>
  <footer class="h-footer text-white">
    <div class="container h-footer__wrapper">
      <div class="row py-4 px-2">
        <div class="col-md-6 mb-md-0 mb-4">
          <div class="d-flex flex-column gap-4">
            <img
              src="/images/logo-white.svg"
              alt="logo satudata banyuwangi"
              loading="eager"
              width="165"
              height="40"
            />
            <p class="h-text-body-16 text-white">
              Eksplorasi bersama data Kabupaten Banyuwangi <br />
              dengan visualisasi yang menarik dan informatif.
            </p>
            <div class="d-block">
              <a href="#" class="h-text-body-16 h-footer__back-top"
                >Kembali ke atas <i class="bi bi-arrow-up"></i
              ></a>
            </div>
          </div>
        </div>
        <div class="col-md-2 mb-md-0 mb-4">
          <h2 class="h-text-body-16 fw-bold mb-3">Menu</h2>
          <ul class="list-unstyled">
            <li v-for="(item, index) in menuItems" :key="index">
              <a :href="item.link" class="h-footer__link h-text-body-16 d-block py-1">
                {{ item.label }}
              </a>
            </li>
          </ul>
        </div>
        <div class="col-md-4 mb-md-0 mb-4">
          <h2 class="h-text-body-16 fw-bold mb-3">Kontak Kami</h2>
          <div class="d-flex flex-column gap-4">
            <div class="d-flex align-items-center gap-2">
              <i class="h-footer__list bi bi-telephone-fill"></i>
              <p class="h-footer__list h-text-body-16 d-block">Telepon:</p>
              <a
                href="tel:+0333424972"
                class="h-footer__link h-text-body-16 d-block"
                >(0333) 424972</a
              >
            </div>
            <div class="d-flex align-items-center gap-2">
              <i class="h-footer__list bi bi-envelope-fill"></i>
              <a
                href="mailto:statistikdansandi@gmail.com"
                class="h-footer__link h-text-body-16 d-block"
                >statistikdansandi@gmail.com</a
              >
            </div>
            <div class="d-flex align-items-start gap-2">
              <i class="h-footer__list bi bi-geo-alt-fill"></i>
              <div class="d-flex flex-column gap-1">
                <p class="h-footer__list h-text-body-16 d-block">
                  Jl. K.H. Agus Salim No.85, Taman Baru,
                </p>
                <p class="h-footer__list h-text-body-16 d-block">
                  Kec. Banyuwangi, Kab. Banyuwangi,
                </p>
                <p class="h-footer__list h-text-body-16 d-block">
                  Jawa Timur 68416.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="h-footer__divider"></div>
      <div class="row py-3">
        <div class="col-md-6 col-lg-8 mb-md-0 mb-4 order-1 order-md-0">
          <p class="h-footer__list h-text-body-16 d-block mb-0">
            Copyright ©2023 Pemerintah Daerah Kabupaten Banyuwangi.
          </p>
        </div>
        <div class="col-md-6 col-lg-4 mb-4 mb-md-0 text-md-right order-0 order-md-1">
          <div class="d-flex gap-2">
            <p class="h-footer__list h-text-body-16 d-block">Follow kami di:</p>
            <div class="d-flex align-items-center gap-3">
              <a v-for="(link, index) in socialMediaLinks" :key="index" :href="link.link" class="text-white opacity-75" rel="noopener noreferrer">
                <i class="h-footer__link" :class="link.iconClass"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
