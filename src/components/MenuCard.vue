<script setup>
const props = defineProps({
  product: {
    type: Object,
  },
});
</script>
<template>
  <div class="card" :class="`${product.available ? '' : 'soldout'}`">
    <div class="tag"><h2>SOLD OUT</h2></div>
    <div class="imagen"><img :src="product.image_url" /></div>
    <div>
      <h1>{{ product.product }}</h1>
      <h2>{{ product.description }}</h2>
      <h3>{{ product.price }}</h3>
    </div>
  </div>
</template>

<style scoped>
.card {
  width: 15.75rem;
  height: 19.75rem;
  border-radius: 3.125rem;
  background: rgba(217, 217, 217, 0.61);
  display: flex;
  text-align: center;
  align-items: center;
  flex-direction: column;
  padding: 2rem;
  position: relative;
  cursor: pointer;
  transition: 0.5s ease;
}

.card:hover {
  background: rgba(217, 217, 217, 0.81);
}

.imagen {
  border-radius: 3.125rem;
  width: 11rem;
  height: 11rem;
  margin-bottom: 1rem;
  overflow: hidden;
}
img {
  object-fit: cover;
  width: 100%;
  height: 100%;
  transition: 0.5s ease;
}

img:hover {
  width: 105%;
  height: 105%;
  transform: translate(-2.5%, -2.5%);
}

h1 {
  font-size: 1rem;
  font-weight: 600;
}

h2 {
  font-size: 1rem;
  font-weight: 200;
}

h3 {
  font-size: 1rem;
  font-weight: 400;
}

.tag {
  display: none;
}

.soldout .tag {
  width: 10rem;
  height: 2.5rem;
  background-color: var(--nodisponible);
  position: absolute;
  left: -40px;
  top: 50px;
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
  color: var(--white);
  z-index: 1;
}

.soldout img {
  filter: grayscale(100%);
}
</style>
