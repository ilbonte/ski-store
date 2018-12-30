<template>
  <div class="ski-store">
    <Product
      class="product"
      :cart="cart"
      v-for="(product) in products"
      :product="product"
      :key="product.key"
    />
  </div>
</template>

<script>
import Product from "./Product.vue";

export default {
  name: "SkiStore",
  props: ["products", "cart"],
  components: {
    Product
  }
};
</script>

<style scoped>
.ski-store {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-evenly;
}
.product {
  margin-bottom: 2em;
}
</style>
