<script setup>
import MiniCard from './MiniCard.vue'
import TagPill from './TagPill.vue'

defineProps({
  companyName: String,
  salary: Number,
  publishDate: String,
  name: String,
  positions: Number,
  modality: String,
  tags: Array
})

</script>

<template>
  <div class="card">
    <img
      src="data:image/png;base64,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"
      alt="company logo"
    />
    <div>
      <div class="card-title-container">
        <p class="card-position">{{ name }}</p>
        <span v-for="tag in tags" :key="tag">
          <TagPill :name="tag" />
        </span>
      </div>
      <div class="card-description-container">
        <MiniCard logoUrl="src/assets/company.svg" :name="companyName" />
        <MiniCard logoUrl="src/assets/location.svg" :name="modality" />
        <MiniCard logoUrl="src/assets/cash.svg" :name="salary" />
        <MiniCard logoUrl="src/assets/people.svg" :name="positions" />
        <MiniCard logoUrl="src/assets/calendar.svg" :name="publishDate" />
      </div>
      <div>
      </div>
    </div>
    <div>
      lorem
    </div>
  </div>
</template>

<style scoped>
.card {
  display: grid;
  align-items: center;
  grid-template-columns: auto 1fr auto;
  column-gap: 12px;
  padding: 4px 12px;
  border-radius: 4px;
  border: 1px solid lightgray;
  background-color: white;
}

img {
  width: 80px;
  height: 80px;
}

.card-title-container {
  display: flex;
  align-items: center;
  column-gap: 12px;
}

.card-position {
  font-weight: 700;
  margin-bottom: 4px;
}

.card-description-container {
  display: flex;
  justify-content: space-between;
  column-gap: 12px;
}
</style>
