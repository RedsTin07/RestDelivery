<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <div class="logo">Rest Delivery Food</div>
  </header>
  <main><RouterView /></main>
  <footer>
    <div>Call to: +41 548 2657 27</div>
    <div>2023</div>
  </footer>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  margin-left: 2rem;
}
</style>
