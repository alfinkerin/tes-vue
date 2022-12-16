<template>
  <div>
    <img class="img-banner" src="~/assets/banner.jpg" />

    <div class="container" v-for="(d, i) in article" :key="i">
      <NuxtLink :to="`/pages/articles/${d.id}`">
        <v-card width="100%">
          <v-card-item>
            <v-card-title>{{ d.title }}</v-card-title>
          </v-card-item>

          <v-card-text> {{ d.body }} </v-card-text>
        </v-card>
      </NuxtLink>
    </div>
    <li class="show"><NuxtLink to="/articles">Show More</NuxtLink></li>
  </div>
</template>

<script setup>
const { data: article } = await useFetch(
  "https://jsonplaceholder.typicode.com/posts?_limit=5"
);
</script>

<style scoped>
.img-banner {
  width: 100%;
  height: 20rem;
}
.container {
  margin: 20px 40px 20px 40px;
}

.show {
  text-decoration: none;
  list-style: none;
  text-align: center;
  font-size: 1em;
}
</style>
