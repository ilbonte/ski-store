<template>
  <div>
    <h1>Welcome to the best ski store</h1>
    <Product name="ski trab"/>
    <Product name="fisher"/>
  </div>
</template>

<script>
import Product from "./Product.vue";

export default {
  name: "SkiStore",
  components: {
    Product
  }
};
</script>

<style>
</style>
