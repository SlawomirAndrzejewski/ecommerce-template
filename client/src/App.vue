<template>
  <div id="wrapper">
    <Navbar :cart="cart" />

    <section class="section">
      <router-view />
    </section>

    {{ cartTotalLength }}

    <footer class="footer">
      <p class="has-text-centered">Copyright (c) 2021 onewebdesign.pl</p>
    </footer>
  </div>
</template>

<script>
import Navbar from "./components/Navbar";

export default {
  name: "App",
  components: {
    Navbar,
  },
  data() {
    return {
      cart: {
        items: [],
      },
      cartLength: 0,
    };
  },
  computed: {
    cartTotalLength() {
      let totalLength = 0;

      for (let i = 0; this.cart.items.length; i++) {
        totalLength += this.cart.items[i].quantity;
      }
      this.cartLength = totalLength;
      return totalLength;
    },
  },
  beforeCreate() {
    this.$store.commit("initializeStore");
  },
  mounted() {
    this.cart = this.$store.state.cart;
    console.log(this.cart.items[0].quantity);
  },
};
</script>

<style lang="scss">
@import "../node_modules/bulma";
</style>
