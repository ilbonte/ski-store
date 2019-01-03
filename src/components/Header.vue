<template>
  <div class="header">
    <h1>{{fongo}}</h1>
    <button id="cart">Items in cart: {{size}}</button>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["cart", "fongo"],
  computed: {
    size: function() {
      //TODO mettere la funzione che calcolza la size su cart
    }
  }
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: flex-end;
}
</style>
