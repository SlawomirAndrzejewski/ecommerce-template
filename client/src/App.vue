<template>
  <div id="wrapper">
    <Navbar />

    <section class="section">
      <router-view />
    </section>

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
};
</script>

<style lang="scss">
@import "../node_modules/bulma";
</style>
