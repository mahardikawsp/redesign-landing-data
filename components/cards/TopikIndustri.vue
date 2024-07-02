<script setup>
const topics = {
  id: "5",
  title: "Industri",
  iconClass: "bi bi-building",
  color: "brown",
  cards: [
    {
      title: "Overview Industri",
      items: [
        { iconClass: "bi bi-eye", value: "150" },
        { iconClass: "bi bi-calendar", value: "2023" },
      ],
    },
    {
      title: "Overview Industri",
      items: [
        { iconClass: "bi bi-eye", value: "126" },
        { iconClass: "bi bi-calendar", value: "2023" },
      ],
    },
    {
      title: "Overview Industri",
      items: [
        { iconClass: "bi bi-eye", value: "126" },
        { iconClass: "bi bi-calendar", value: "2023" },
      ],
    },
  ],
};
</script>

<template>
  <div class="h-card-outline mb-4">
    <div class="d-flex align-items-center gap-3">
      <div
        :class="['h-tabs-button__icon', `h-tabs-button__icon--${topics.color}`]"
      >
        <i :class="topics.iconClass"></i>
      </div>
      <span class="fw-semibold">{{ topics.title }}</span>
    </div>
    <div class="row">
      <div v-for="(topic, i) in topics.cards" :key="i" class="col-md-6 col-lg-3">
        <div class="h-card-outline h-card-outline--overview mt-4">
          <div class="d-flex flex-column gap-3">
            <div class="h-card__icon h-card__icon--grayscale">
              <div class="h-card__icon-inner"></div>
            </div>
            <p class="h-text-body-16 fw-semibold">{{ topic.title }}</p>
          </div>
          <div class="d-flex align-items-center gap-2">
            <div
              v-for="(item, i) in topic.items"
              :key="i"
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
