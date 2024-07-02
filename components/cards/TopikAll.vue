<script setup>
const topics = [
  {
    id: "2",
    title: "Sosial",
    iconClass: "bi bi-person-check",
    color: "green",
    cards: [
      {
        title: "Overview Sosial",
        items: [
          { iconClass: "bi bi-eye", value: "126" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
      {
        title: "Overview Sosial",
        items: [
          { iconClass: "bi bi-eye", value: "126" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
    ],
  },
  {
    id: "3",
    title: "Kesehatan",
    iconClass: "bi bi-heart-pulse",
    color: "maroon",
    cards: [
      {
        title: "Overview Kesehatan",
        items: [
          { iconClass: "bi bi-eye", value: "150" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
      {
        title: "Overview Sosial",
        items: [
          { iconClass: "bi bi-eye", value: "126" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
      {
        title: "Overview Sosial",
        items: [
          { iconClass: "bi bi-eye", value: "126" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
    ],
  },
  {
    id: "4",
    title: "Kependudukan",
    iconClass: "bi bi-people",
    color: "navy",
    cards: [
      {
        title: "Overview Sosial",
        items: [
          { iconClass: "bi bi-eye", value: "126" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
    ],
  },
  {
    id: "5",
    title: "Industri",
    iconClass: "bi bi-building",
    color: "brown",
    cards: [
      {
        title: "Overview Kesehatan",
        items: [
          { iconClass: "bi bi-eye", value: "150" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
    ],
  },
  {
    id: "6",
    title: "Pendidikan",
    iconClass: "bi bi-mortarboard",
    color: "purple",
    cards: [
      {
        title: "Overview Sosial",
        items: [
          { iconClass: "bi bi-eye", value: "126" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
      {
        title: "Overview Sosial",
        items: [
          { iconClass: "bi bi-eye", value: "126" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
    ],
  },
  {
    id: "7",
    title: "Ekonomi dan Keuangan",
    iconClass: "bi bi-bar-chart-line",
    color: "pink",
    cards: [
      {
        title: "Overview Sosial",
        items: [
          { iconClass: "bi bi-eye", value: "126" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
    ],
  },
  {
    id: "8",
    title: "Lingkungan Hidup",
    iconClass: "bi bi-tree",
    color: "ivory",
    cards: [
      {
        title: "Overview Kesehatan",
        items: [
          { iconClass: "bi bi-eye", value: "150" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
      {
        title: "Overview Sosial",
        items: [
          { iconClass: "bi bi-eye", value: "126" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
    ],
  },
  {
    id: "9",
    title: "Kemiskinan",
    iconClass: "bi bi-graph-down-arrow",
    color: "green",
    cards: [
      {
        title: "Overview Kesehatan",
        items: [
          { iconClass: "bi bi-eye", value: "150" },
          { iconClass: "bi bi-calendar", value: "2023" },
        ],
      },
    ],
  },
];
</script>

<template>
  <div v-for="(topic, i) in topics" :key="i" class="h-card-outline mb-4">
    <div class="d-flex align-items-center gap-3">
      <div
        :class="['h-tabs-button__icon', `h-tabs-button__icon--${topic.color}`]"
      >
        <i :class="topic.iconClass"></i>
      </div>
      <span class="fw-semibold">{{ topic.title }}</span>
    </div>
    <div class="row">
      <div v-for="(card, i) in topic.cards" :key="i" class="col-md-6 col-lg-3">
        <div class="h-card-outline h-card-outline--overview mt-4">
          <div class="d-flex flex-column gap-3">
            <div class="h-card__icon h-card__icon--grayscale">
              <div class="h-card__icon-inner"></div>
            </div>
            <p class="h-text-body-16 fw-semibold">{{ card.title }}</p>
          </div>
          <div class="d-flex align-items-center gap-2">
            <div
              v-for="(item, j) in card.items"
              :key="j"
              class="d-flex align-items-center gap-2 border rounded-2 px-2 py-1"
            >
              <i :class="item.iconClass"></i>
              <span class="h-text-body-12 h-text-secondary">{{
                item.value
              }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
