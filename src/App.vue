<template>
  <div id="app">
    <Header :cart="cart"></Header>
    <SkiStore :products="products" :cart="cart"/>
    <Footer></Footer>
  </div>
</template>

<script>
import SkiStore from "./components/SkiStore.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import products from "./assets/products.json";
let cart = [];
export default {
  name: "app",
  components: {
    SkiStore,
    Header,
    Footer
  },
  data: function() {
    return { products, cart };
  }
};
</script>

<style>
</style>
