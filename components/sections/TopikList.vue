<script setup>
const topics = [
  { id: "1", label: "Semua Topik", icon: "grid", color: "dark" },
  { id: "2", label: "Sosial", icon: "person-check", color: "green" },
  {
    id: "3",
    label: "Kesehatan",
    icon: "heart-pulse",
    color: "maroon",
  },
  { id: "4", label: "Kependudukan", icon: "people", color: "navy" },
  { id: "5", label: "Industri", icon: "building", color: "brown" },
  {
    id: "6",
    label: "Pendidikan",
    icon: "mortarboard",
    color: "purple",
  },
  {
    id: "7",
    label: "Ekonomi dan Keuangan",
    icon: "bar-chart-line",
    color: "pink",
  },
  {
    id: "8",
    label: "Lingkungan Hidup",
    icon: "tree",
    color: "ivory",
  },
  {
    id: "9",
    label: "Kemiskinan",
    icon: "graph-down-arrow",
    color: "green",
  },
];
let activeTab = 0;

const menuActive = ref(false);
const selectedOption = ref("Pilih topik yang disukai");
const selectedIcon = ref("");
const selectedColor = ref("");

const toggleMenu = () => {
  menuActive.value = !menuActive.value;
};

const selectOption = (option) => {
  selectedOption.value = option.label;
  selectedIcon.value = option.icon;
  selectedColor.value = option.color;
  menuActive.value = false;
};
</script>

<template>
  <section class="h-section">
    <div class="row">
      <div class="col-md-4 col-lg-3">
        <!-- Mobile Only -->
        <div
          class="h-dropdown d-block d-md-none"
          :class="{ active: menuActive }"
        >
          <div class="h-dropdown-select" @click="toggleMenu">
            <div class="d-flex align-items-center gap-2">
              <i
                :class="`bi bi-${selectedIcon}`"
                :style="{ color: selectedColor }"
              ></i>
              <span class="sBtn-text">{{ selectedOption }}</span>
            </div>
            <i class="bi bi-chevron-down"></i>
          </div>

          <ul class="h-dropdown-options">
            <li
              v-for="option in topics"
              :key="option.id"
              class="h-dropdown-option"
              @click="selectOption(option)"
            >
              <i
                :class="`bi bi-${option.icon}`"
                :style="{ color: option.color }"
              ></i>
              <span class="h-dropdown-option-text">{{ option.label }}</span>
            </li>
          </ul>
        </div>
        <!-- Desktop Only -->
        <div class="d-none d-md-block">
          <div
            class="nav flex-column align-items-start nav-pills me-3"
            role="tablist"
            aria-orientation="vertical"
          >
            <button
              v-for="(topic, index) in topics"
              :key="index"
              class="h-tabs-button nav-link"
              :class="{ active: index === activeTab }"
              :id="`v-pills-${index + 1}-tab`"
              data-bs-toggle="pill"
              :data-bs-target="`#v-pills-${index + 1}`"
              type="button"
              role="tab"
              :aria-controls="`v-pills-${index + 1}`"
              :aria-selected="index === activeTab"
            >
              <div
                :class="[
                  'h-tabs-button__icon',
                  `h-tabs-button__icon--${topic.color}`,
                ]"
              >
                <i :class="`bi bi-${topic.icon}`"></i>
              </div>
              <span>{{ topic.label }}</span>
            </button>
          </div>
        </div>
        <div class="h-card-shadow h-card-shadow--soft d-none d-md-block mt-4">
          <div class="d-flex flex-column gap-3">
            <i
              class="bi bi-file-earmark-arrow-up-fill h-text-heading-36 h-text-blue"
            ></i>
            <p class="h-text-heading-16">Perlu topik lainnya?</p>
            <p class="h-text-body-14 mb-3">
              Anda bisa request topik lain yang sifatnya tidak terbuka.
            </p>
            <button
              class="h-btn--primary"
              data-bs-toggle="modal"
              data-bs-target="#modalTopik"
            >
              Request Topik
            </button>
          </div>
        </div>
      </div>
      <div class="col-md-8 col-lg-9">
        <div
          class="d-flex flex-column flex-md-row justify-content-between align-items-md-center gap-3 my-4"
        >
          <h2 class="h-text-heading-24">Daftar Topik</h2>
          <div class="col-lg-4">
            <div class="input-group-lg position-relative">
              <label
                for="exampleFormControlInput1"
                class="sr-only d-none visually-hidden"
                >Cari Topik</label
              >
              <input
                type="text"
                class="h-input-search h-input-search--md form-control rounded"
                id="exampleFormControlInput1"
                placeholder="Cari Topik"
              />
              <button
                class="h-input-search__button h-btn--primary h-btn--xs rounded"
              >
                Cari
              </button>
            </div>
          </div>
        </div>
        <div class="tab-content" id="v-pills-tabContent">
          <div
            v-for="(tab, index) in topics"
            :key="index"
            :class="{ 'show active': index === activeTab }"
            class="tab-pane fade"
            :id="`v-pills-${index + 1}`"
            role="tabpanel"
            :aria-labelledby="`v-pills-${index + 1}-tab`"
          >
            <CardsTopikAll v-if="tab.id === '1'" />
            <CardsTopikSosial v-if="tab.id === '2'" />
            <CardsTopikKesehatan v-if="tab.id === '3'" />
            <CardsTopikKependudukan v-if="tab.id === '4'" />
            <CardsTopikIndustri v-if="tab.id === '5'" />
            <CardsTopikPendidikan v-if="tab.id === '6'" />
            <CardsTopikEkonomi v-if="tab.id === '7'" />
            <CardsTopikLingkungan v-if="tab.id === '8'" />
            <CardsTopikKemiskinan v-if="tab.id === '9'" />
            <CardsTopikSosial v-if="tab.id === '10'" />
          </div>
        </div>
        <div class="h-card-shadow h-card-shadow--soft d-block d-md-none mt-4">
          <div class="d-flex flex-column gap-3">
            <i
              class="bi bi-file-earmark-arrow-up-fill h-text-heading-36 h-text-blue"
            ></i>
            <p class="h-text-heading-16">Perlu topik lainnya?</p>
            <p class="h-text-body-14 mb-3">
              Anda bisa request topik lain yang sifatnya tidak terbuka.
            </p>
            <button
              class="h-btn--primary"
              data-bs-toggle="modal"
              data-bs-target="#modalTopik"
            >
              Request Topik
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
  <ModalsTopik />
</template>

<style scoped>
.nav-pills .nav-link.active {
  background-color: var(--soft) !important;
  border-top-left-radius: 0 !important;
  border-bottom-left-radius: 0 !important;
  border-top-right-radius: 0.75rem !important;
  border-bottom-right-radius: 0.75rem !important;
  border-left: 2px solid var(--blue) !important;
  color: var(--blue) !important;
  font-weight: 600;
}
</style>
