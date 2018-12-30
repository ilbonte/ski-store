<template>
  <div id="app">
    <Header></Header>
    <SkiStore :products="products"/>
    <Footer></Footer>
  </div>
</template>

<script>
import SkiStore from "./components/SkiStore.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import products from "./assets/products.json";

export default {
  name: "app",
  components: {
    SkiStore,
    Header,
    Footer
  },
  data: function() {
    return { products: products };
  }
};
</script>

<style>
</style>
