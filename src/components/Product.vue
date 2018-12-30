<template>
  <div class="product-box">
    <h1>{{product.name}}</h1>
    <img src="../assets/logo.png" alt="logo">
    <p>{{product.description}}</p>
    <h3>{{product.price}} €</h3>
    <button
      @click="addToCart()"
      :class="{disabledButton:notAvailable, 'disabled':notAvailable}"
    >Add to cart</button>
    <span>Available: {{product.quantity}}</span>
  </div>
</template>

<script>
let notAvailable = false;
export default {
  props: ["product", "cart"],
  methods: {
    addToCart: function() {
      if (this.product.quantity > 0) {
        this.product.quantity -= 1;
        this.cart.push(this.product.key);
      }
    }
  },
  computed: {
    notAvailable: function() {
      return this.product.quantity < 1;
    }
  }
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
.disabledButton {
  background: gray;
}

.disabledButton:hover {
  cursor: not-allowed;
}
</style>
