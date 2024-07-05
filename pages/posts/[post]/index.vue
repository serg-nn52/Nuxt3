<template>
  <div>Dinamic post</div>
</template>

<script setup lang="ts">
const route = useRoute();

console.log(route);
</script>

<style scoped>
div {
  font-size: 40px;
  font-weight: 700;
  color: green;
}
</style>
