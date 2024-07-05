<template>
  <div>
    Posts Page

    <div v-if="status === 'pending'">Loading...</div>
    <div v-else class="posts" v-for="post in posts" :key="post.id">
      {{ post.title }}
    </div>
  </div>
</template>

<script setup lang="ts">
definePageMeta({ layout: "posts" });

// const posts = ref<any[]>([]);

// try {
//   const data = await fetch("https://jsonplaceholder.typicode.com/posts");
//   posts.value = await data.json();
// } catch (e) {
//   console.error(e);
// }

//useFetch, useAsyncData

const {
  data: posts,
  error,
  status,
} = useLazyFetch<any[]>("https://jsonplaceholder.typicode.com/posts");

watchEffect(() => {
  console.log(status.value);
});
</script>

<style scoped>
div {
  font-size: 40px;
  font-weight: 700;
  color: green;
}
.posts {
  color: black;
  font-weight: 500;
  font-size: 24px;
}
</style>
