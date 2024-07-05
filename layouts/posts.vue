<template>
  <div class="wrapper">
    <header>Posts Header</header>
    <AppMenu />
    <div class="container">
      <slot />
    </div>
    <footer>Posts Footer</footer>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  min-height: 100dvh;
  justify-content: space-between;
}
.container {
  flex-grow: 1;
}
header,
footer {
  height: 100px;
  background-color: lightgrey;
  color: red;
  font-size: 32px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
