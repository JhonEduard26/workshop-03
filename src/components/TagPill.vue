<script setup>

defineProps({
  name: String
})

</script>

<template>
  <div>
    <span>
      {{ name }}
    </span>
  </div>
</template>

<style scoped>
div {
  display: inline-flex;
  width: max-content;
  padding: 4px 8px;
  border-radius: 6px;
  border: 1px solid lightgray;
  background-color: white;
}

div span {
  font-size: 0.85rem;
}
</style>
