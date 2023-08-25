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
  imgUrl: String,
  tags: Array
})

</script>

<template>
  <div class="card">
    <img :src="imgUrl" alt="company logo" />
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
        <MiniCard logoUrl="src/assets/cash.svg" :name="'$ ' + salary + ' COP'" />
        <MiniCard logoUrl="src/assets/people.svg" :name="positions + ' vacantes'" />
        <MiniCard logoUrl="src/assets/calendar.svg" :name="publishDate" />
        <div class="card-benefits">
          <img class="card-icon" src="../assets/award.svg" alt="award logo" title="Premios" />
          <img class="card-icon" src="../assets/sport.svg" alt="sport logo" title="Recreación " />
          <img class="card-icon" src="../assets/party.svg" alt="party logo" title="Fiesta de fin de año" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card {
  overflow-x: hidden;
  display: grid;
  align-items: center;
  grid-template-columns: auto 1fr auto;
  column-gap: 12px;
  padding: 12px;
  border-radius: 4px;
  border: 1px solid lightgray;
  background-color: white;
}

.card > img {
  width: 80px;
  height: 80px;
}

.card-title-container {
  display: flex;
  align-items: center;
  column-gap: 12px;
  margin-bottom: 12px;
}

.card-position {
  font-weight: 700;
}

.card-description-container {
  display: grid;
  grid-auto-flow: column;
}

.card-benefits {
  display: inline-flex;
  column-gap: 4px;
}

.card-benefits img {
  padding: 4px;
  border-radius: 100%;
  border: 1px solid lightgray;
}

@media (width <=580px) {
  .card-description-container {
    display: none;
  }
}
</style>
