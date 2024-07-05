<template>
  <nav>
    <NuxtLink :to="{ path: '/' }" class="link">Home</NuxtLink>
    <NuxtLink :to="{ path: '/posts' }" class="link">Posts</NuxtLink>
  </nav>
</template>

<script setup lang="ts"></script>

<style scoped>
.link {
  padding: 10px;
}
</style>
