<template>
  <div>
    <Product name="ski trab"/>
    <Product name="fisher"/>
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
