<template>
  <div>
    <header>
      <ul class="navbar">
        <li class="menu"><NuxtLink to="/">Home</NuxtLink></li>
        <li class="menu"><NuxtLink to="/articles">Article</NuxtLink></li>
      </ul>
    </header>

    <div>
      <slot />
    </div>

    <footer>
      <span>created by alfin kerin saputra</span>
    </footer>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.router-link-exact-active {
  color: rgb(26, 210, 84);
}
.navbar {
  display: flex;
  justify-content: end;
  padding: 10px;
  list-style: none;
}

.menu {
  margin: 0 10px;
}
</style>
