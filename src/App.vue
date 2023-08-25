<script setup>
import { jobs } from './data.json'
import JobCard from './components/JobCard.vue'
import MainFooter from './components/MainFooter.vue'
</script>

<template>
  <main>
    <div v-for="job in jobs" :key="job.id">
      <JobCard :companyName="job.company" :salary="job.salary" :publishDate="job.date" :name="job.name"
        :positions="job.positions" :modality="job.modality" :imgUrl="job.imgUrl" :tags="job.tags" />
    </div>
  </main>
  <MainFooter />
</template>

<style scoped>
main {
  max-width: 88%;
  margin: auto;
  margin-bottom: 88px;
}

div {
  margin-bottom: 24px;
}

div:hover {
  cursor: pointer;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.25)
}
</style>
