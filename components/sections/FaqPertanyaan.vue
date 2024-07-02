<script setup>
const accordionItems = ref([
  {
    question:
      "Bagaimana jika kami ingin mengetahui jadwal rilis data yang terdapat di Banyuwangi Satu Data?",
    answer: "Terdapat jadwal rilis data yang dapat didownload disini.",
  },
  {
    question:
      "Bagaimana jika kami ingin mengetahui secara singkat dan ringkas terkait Website Banyuwangi Satu Data?",
    answer:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  },
  {
    question: "Apakah Kabupaten Banyuwangi telah memiliki SOP terkait data?",
    answer:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  },
  {
    question:
      "Apakah Kabupaten Banyuwangi telah memiliki peraturan terkait pengelolaan data?",
    answer:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  },
  {
    question:
      "Apakah data yang ditampilkan pada Portal Satu Data Banyuwangi dapat dipercaya?",
    answer:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  },
  {
    question: "Apa langkah selanjutnya jika kami telah melakukan Request Data?",
    answer:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  },
  {
    question:
      "Bagaimana jika data yang saya cari tidak tersedia pada Portal Satu Data Banyuwangi?",
    answer:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  },
]);
</script>

<template>
  <section class="h-section h-section__floating">
    <div class="container position-relative">
      <img src="/images/icon/wafe.svg" class="h-section-faq h-section-faq--icon-left img-fluid" loading="lazy" alt="wafe">
      <div class="row justify-content-center mt-5 mt-md-0">
        <div class="col-md-11 col-lg-9">
          <div class="accordion accordion-flush" id="accordion-list">
            <div
              v-for="(item, index) in accordionItems"
              :key="index"
              class="h-accordion-item accordion-item"
            >
              <h2 class="h-accordion-header accordion-header">
                <button
                  class="h-text-heading-18 h-accordion-button accordion-button pe-5 collapsed"
                  type="button"
                  :data-bs-toggle="'collapse'"
                  :data-bs-target="'#accordion-content-' + (index + 1)"
                >
                  {{ item.question }}
                </button>
              </h2>
              <div
                :id="'accordion-content-' + (index + 1)"
                class="accordion-collapse collapse"
                data-bs-parent="#accordion-list"
              >
                <div class="h-accordion-body accordion-body">
                  <p class="mb-3">{{ item.answer }}</p>
                  <button class="h-btn-outline--primary">
                    <i class="h-text-blue fw-bold bi bi-download"></i>
                    Download file
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <img src="/images/icon/double-line.svg" class="h-section-faq h-section-faq--icon-right img-fluid" loading="lazy" alt="line">
    </div>
  </section>
</template>
