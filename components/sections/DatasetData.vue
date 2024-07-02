<script setup>
const tabs = [
  { id: "1", label: "Standar Data" },
  { id: "2", label: "Meta Data" },
  { id: "3", label: "Kode Referensi" },
  { id: "4", label: "Interoperabilitas" },
];

let activeTab = 0;

const setActiveTab = (index) => {
  activeTab = index;
};
</script>

<template>
  <div class="mt-5">
    <ul class="nav flex-nowrap nav-pills mb-3 border-bottom border-1 overflow-x-scroll overflow-y-hidden" role="tablist">
      <li
        v-for="(tab, index) in tabs"
        :key="index"
        class="nav-item"
        role="presentation"
      >
        <button
          :class="[
            'nav-link tab-link position-relative',
            { active: activeTab === index },
          ]"
          :id="`pills-${tab.id}-tab`"
          data-bs-toggle="pill"
          :data-bs-target="`#pills-${tab.id}`"
          type="button"
          role="tab"
          :aria-controls="`pills-${tab.id}`"
          :aria-selected="activeTab === index"
          @click="setActiveTab(index)"
        >
          {{ tab.label }}
        </button>
      </li>
    </ul>
    <div
      class="tab-content h-card-outline"
      id="pills-tabContent"
    >
      <div
        v-for="(tab, index) in tabs"
        :key="index"
        :class="[
          'tab-pane',
          'fade',
          { show: activeTab === index, active: activeTab === index },
        ]"
        :id="`pills-${tab.id}`"
        role="tabpanel"
        :aria-labelledby="`pills-${tab.id}-tab`"
      >
        <SectionsDatasetStandarData v-if="tab.id === '1'" />
        <SectionsDatasetMetaData v-if="tab.id === '2'" />
        <SectionsDatasetKodeReferensi v-if="tab.id === '3'" />
        <SectionsDatasetInteroperabilitas v-if="tab.id === '4'" />
      </div>
    </div>
  </div>
</template>
