<script setup>
import { useRoute } from "vue-router";
const route = useRoute();

const menuLinksLogin = ref([
  { to: "/", label: "Beranda" },
  { to: "/dataset", label: "Dataset" },
  { to: "/organisasi", label: "Organisasi" },
  { to: "/publikasi", label: "Publikasi" },
  { to: "/faq", label: "FAQ" },
]);

const menuLinks = ref([
  { to: "/", label: "Beranda" },
  { to: "/dataset", label: "Dataset" },
  { to: "/open-data", label: "Open Data" },
  { to: "/topik", label: "Topik" },
]);
</script>

<template>
  <nav
    v-if="route.path === '/login'"
    class="d-flex h-navbar navbar navbar-expand-md position-relative navbar-expand-md p-3 p-lg-0"
  >
    <div class="col-md-6 h-login-left">
      <NuxtLink to="/" class="navbar-brand">
        <img
          src="/images/logo.svg"
          alt="logo satudata banyuwangi"
          loading="eager"
          width="165"
          height="40"
        />
      </NuxtLink>
    </div>
    <div class="col-md-6 h-login-right">
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="offcanvas"
        data-bs-target="#offcanvasNavbar"
        aria-controls="offcanvasNavbar"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="currentColor"
          class="bi bi-list"
          viewBox="0 0 16 16"
        >
          <path
            fill-rule="evenodd"
            d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"
          />
        </svg>
      </button>
      <div
        class="offcanvas offcanvas-end"
        tabindex="-1"
        id="offcanvasNavbar"
        aria-labelledby="offcanvasNavbarLabel"
      >
        <div class="offcanvas-header">
          <NuxtLink to="/" id="offcanvasNavbarLabel" class="navbar-brand">
            <img
              src="/images/logo.svg"
              alt="logo satudata banyuwangi"
              loading="eager"
              width="165"
              height="40"
            />
          </NuxtLink>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="offcanvas"
            aria-label="Close"
          ></button>
        </div>
        <div class="offcanvas-body">
          <ul class="navbar-nav justify-content-end flex-grow-1">
            <li
              v-for="menu in menuLinksLogin"
              :key="menu.label"
              class="nav-item"
            >
              <NuxtLink
                :to="menu.to"
                :class="{ active: menu.to === route.path }"
                aria-current="page"
                :exact="true"
                class="h-navbar__link nav-link"
              >
                {{ menu.label }}
              </NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
  <nav v-else class="h-navbar navbar navbar-expand-md position-relative">
    <div class="container py-2">
      <NuxtLink to="/" class="navbar-brand">
        <img
          src="/images/logo.svg"
          alt="logo satudata banyuwangi"
          loading="eager"
          width="165"
          height="40"
        />
      </NuxtLink>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="offcanvas"
        data-bs-target="#offcanvasNavbar"
        aria-controls="offcanvasNavbar"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="currentColor"
          class="bi bi-list"
          viewBox="0 0 16 16"
        >
          <path
            fill-rule="evenodd"
            d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"
          />
        </svg>
      </button>
      <div
        class="offcanvas offcanvas-end"
        tabindex="-1"
        id="offcanvasNavbar"
        aria-labelledby="offcanvasNavbarLabel"
      >
        <div class="offcanvas-header">
          <NuxtLink to="/" id="offcanvasNavbarLabel" class="navbar-brand">
            <img
              src="/images/logo.svg"
              alt="logo satudata banyuwangi"
              loading="eager"
              width="165"
              height="40"
            />
          </NuxtLink>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="offcanvas"
            aria-label="Close"
          ></button>
        </div>
        <div class="offcanvas-body">
          <ul class="navbar-nav justify-content-end flex-grow-1">
            <li v-for="menu in menuLinks" :key="menu.label" class="nav-item">
              <NuxtLink
                :to="menu.to"
                :class="{ active: menu.to === route.path }"
                aria-current="page"
                :exact="true"
                class="h-navbar__link nav-link"
              >
                {{ menu.label }}
              </NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>
