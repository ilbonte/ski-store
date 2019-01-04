<template>
  <div class="cartPopup">
    <h1>carrello</h1>
    <h2>{{cart}}</h2>
    <ul>
      <li
        v-for="(value,key) in cart"
        :key="`chiave-${key}`"
      >{{getProductFromKey(key).name}} -> {{value}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["cart", "products"],

  methods: {
    getProductFromKey: function(key) {
      for (var product of this.products) {
        if (product.key == key) {
          return product;
        }
      }
    }
  }
};
</script>

<style scoped>
.cartPopup {
  width: 200px;
  background-color: aquamarine;
  max-height: 150px;
  overflow-y: scroll;
}
</style>
