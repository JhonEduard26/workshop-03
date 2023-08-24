<script setup>
import { jobs } from './data.json'
import JobCard from './components/JobCard.vue'
</script>

<template>
  <div v-for="job in jobs" :key="job.id">
    <JobCard
      :companyName="job.company"
      :salary="job.salary"
      :publishDate="job.date"
      :name="job.name"
      :positions="job.positions"
      :tags="job.tags"
    />
  </div>
</template>

<style scoped></style>
