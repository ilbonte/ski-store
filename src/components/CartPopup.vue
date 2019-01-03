<template>
  <div>
    <h1>carrello</h1>
    <h2>{{cart}}</h2>
    <ul>
      <li v-for="(value,key) in cart" :key="`chiave-${key}`">{{getProductFromKey(key)}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["cart", "products"],

  methods: {
    getProductFromKey: function(key) {
      console.log(this.products);

      for (var product of this.products) {
        console.log(product);
        if (product.key == key) {
          return product;
        }
      }
    }
  }
};
</script>

<style>
</style>
