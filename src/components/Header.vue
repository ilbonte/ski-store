<template>
  <div class="header">
    <button id="cart">Items in cart: {{cart.length}}</button>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["cart"]
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: flex-end;
}
</style>
