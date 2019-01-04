<template>
  <div class="header">
    <span>Ski store</span>
    <button id="cart" @click="$emit('toggleCart')">Items in cart: {{cartSize}}</button>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["cart"],
  computed: {
    cartSize: function() {
      const values = Object.values(this.cart);
      return values.reduce((a, b) => a + b, 0);
    }
  }
};
</script>

<style scoped>
.header {
  background-color: #6fbe92;
}
</style>
