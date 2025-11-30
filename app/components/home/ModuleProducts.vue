<script setup lang="ts">
import CardProduct from '@/components/product/CardProduct.vue';
</script>

<template>
  <div class="module-products-container">
    <h1>Products</h1>
    <h2>Order it for you or for your beloved ones </h2>

    <CardProduct/>
  </div>
</template>

<style scoped>

.module-products-container {
  width: 100%;
  padding: 2rem;
  display: flex;
  flex-direction: column ;
  height: auto; ;
}

.module-products-container h1,h2 {
  text-align: center;
}
</style>