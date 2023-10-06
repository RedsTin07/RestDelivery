<script setup>
import MenuCard from "./MenuCard.vue";
import { products } from "./../database/card_database";
</script>
<template>
  <div class="cards-container">
    <MenuCard v-for="dbp in products" :product="dbp" />
  </div>
</template>

<style scoped>
.cards-container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  justify-items: center;
  gap: 2rem;
  margin-left: 8rem;
  margin-right: 8rem;
  margin-top: 1rem;
  margin-bottom: 1rem;
  transition-property: font-size;
  transition-duration: 0.7s;
  transition: 300ms;
}

@media screen and (max-width: 1400px) {
  .cards-container {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media screen and (max-width: 1150px) {
  .cards-container {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media screen and (max-width: 830px) {
  .cards-container {
    grid-template-columns: repeat(1, 1fr);
    margin-left: 5rem;
  }
}
@media screen and (max-width: 830px) {
  .cards-container {
    grid-template-columns: repeat(1, 1fr);
    margin-left: 4rem;
  }
}
</style>
