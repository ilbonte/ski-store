<template>
  <div>
    <Product v-for="(product) in products" :product="product" :key="product.key"/>
  </div>
</template>

<script>
import Product from "./Product.vue";

export default {
  name: "SkiStore",
  props: ["products"],
  components: {
    Product
  }
};
</script>

<style>
</style>
