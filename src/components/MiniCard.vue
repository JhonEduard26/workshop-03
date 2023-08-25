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
  column-gap: 4px;
}
.card-icon {
  width: 20px;
  height: 20px;
}
</style>
