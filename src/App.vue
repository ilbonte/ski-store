<template>
  <div id="app">
    <Header :cart="cart" @toggleCart="toggleCart"></Header>
    <CartPopup :cart="cart" :products="products" v-show="showCart"/>
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
  methods: {
    toggleCart: function() {
      this.showCart = !this.showCart;
    }
  },
  data: function() {
    return { products, cart: {}, showCart: false };
  }
};
</script>
<style>
.ski-store {
  margin-top: 3em;
}
.header {
  position: fixed;
  font-size: 2em;
  top: 0px;
  right: 100px;
}
.cartPopup {
  position: fixed;
  font-size: 2em;
  top: 35px;
  right: 100px;
}
</style>
