<template>
  <div class="product-box">
    <h1>{{product.name}}</h1>
    <img src="../assets/logo.png" alt="logo">
    <p>{{product.description}}</p>
    <h3>{{product.price}} €</h3>
    <button>Add to cart</button>
  </div>
</template>

<script>
export default {
  props: ["product"]
};
</script>

<style scoped>
.product-box {
  flex: 0 1 20%;
  min-width: 250px;
  text-align: center;
  border: 1px grey solid;
  box-shadow: 2px 2px 2px 0px rgba(53, 73, 93, 0.8);
  padding-bottom: 2em;
}
.product-box:hover {
  box-shadow: 2px 2px 2px 0px rgb(64, 184, 131);
}

button {
  font-size: 1em;
  padding: 0.5em;
  background: #40b883;
  color: white;
}
button:hover {
  cursor: pointer;
}
</style>
