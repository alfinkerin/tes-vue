<template>
  <div>
    <div class="container">
      <img class="gambar" :src="image.url" />
      <h1>{{ isi.title }}</h1>

      <p>{{ isi.body }}</p>

      <Share />
    </div>
  </div>
</template>

<script setup>
const { id } = useRoute().params;

const { data: isi } = await useFetch(
  `https://jsonplaceholder.typicode.com/posts/${id}`
);

const { data: image } = await useFetch(
  `https://jsonplaceholder.typicode.com/photos/${id}`
);
</script>

<style scoped>
.container {
  margin: 2rem;
}
.gambar {
  width: 100%;
  height: 15rem;
}
</style>
