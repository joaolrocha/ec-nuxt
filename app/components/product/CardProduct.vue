<script setup lang="ts">

</script>

<template>
    <div class="card-product-content">
      <div class="image-container">
      <NuxtImg class="product-image" src="/product.svg" alt="Product Image" width="300" height="200" />
      </div>
      <div class="card-product-details">
        <h2 class="card-product-title">Product Title</h2>
        <div class="card-product-price">$99.99</div>
        <!-- <button class="card-product-button">Add to Cart</button> -->
      </div>
    </div>
</template>

<style scoped>
.card-product-content{
  display: flex;
  width: 255px;;
  flex-direction: column;
  align-items: center;
  box-shadow: 0 6px 6px rgba(0, 0, 0, 0.1);
  /* border: 1px solid #e0e0e0; */
}

.image-container{
  background-color: #F7F8FA;
  width: 100%;
  display: flex;
  justify-content: center ;
  /* align-items: center; */
}

.card-product-details{
  width: 100%;
  display: flex;
  flex-direction: column;
}

.card-product-title {
  font-size: 1.2rem;
  margin: 0.5rem 0;
  padding: 0 1rem;
}

.card-product-price {
  text-align: end;
  font-size: 1.2rem;
  margin: 0.5rem 0;
  padding: 0 1rem;
}
</style>