<template>
  <div>
    <div class="">
      <div class="container" v-for="(d, i) in article" :key="i">
        <NuxtLink :to="`/articles/${d.id}`">
          <v-card width="100%">
            <v-card-item>
              <v-card-title>{{ d.title }}</v-card-title>
            </v-card-item>

            <v-card-text> {{ d.body }} </v-card-text>
          </v-card>
        </NuxtLink>
      </div>
    </div>
    <Pagination />
  </div>
</template>

<script setup>
definePageMeta({
  layout: "default",
});

const { data: article } = await useFetch(
  "https://jsonplaceholder.typicode.com/posts?_limit=10"
);
</script>

<style scoped>
.container {
  margin: 10px;
}
</style>
