<script setup>

defineProps({
  name: String,
  logoUrl: String
})

</script>

<template>
  <p>
    <img class="card-icon" :src="logoUrl" :alt="name" />
    {{ name }}
  </p>
</template>

<style scoped>
p {
  display: inline-flex;
  align-items: center;
  column-gap: 2px;
  font-size: 0.85rem;
}
</style>
