<template>
  <div>
    <h2>Loxa de produtos</h2>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products">
        <ProductCard :product='p' />
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products',
});

// fetch the products
const { data: products } = await useFetch('https://fakestoreapi.com/products');
</script>

<style scoped></style>
