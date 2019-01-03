<template>
  <div id="app">
    <Header :cart="cart"></Header>
    <CartPopup :cart="cart" :products="products"/>
    <SkiStore :products="products" :cart="cart"/>
    <Footer></Footer>
  </div>
</template>

<script>
import SkiStore from "./components/SkiStore.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import CartPopup from "./components/CartPopup.vue";
import products from "./assets/products.json";

export default {
  name: "app",
  components: {
    SkiStore,
    Header,
    Footer,
    CartPopup
  },
  data: function() {
    return { products, cart: {} };
  }
};
</script>

<style>
</style>
