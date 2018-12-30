<template>
  <div class="header">
    <span id="cart">Items in cart: {{cart.length}}</span>
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
