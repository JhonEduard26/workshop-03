<script setup>
import { jobs } from './data.json'
import JobCard from './components/JobCard.vue'
</script>

<template>
  <main>
    <div v-for="job in jobs" :key="job.id">
      <JobCard :companyName="job.company" :salary="job.salary" :publishDate="job.date" :name="job.name"
        :positions="job.positions" :modality="job.modality" :tags="job.tags" />
    </div>
  </main>
</template>

<style scoped>
main {
  max-width: 88%;
  margin: auto;
}

div {
  margin-bottom: 24px;
}

div:hover {
  cursor: pointer;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.25)
}
</style>
