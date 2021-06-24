<template>
  <nav class="navbar is-dark">
    <div class="navbar-brand">
      <router-link to="/" class="navbar-item">
        <strong>OneShop</strong>
      </router-link>

      <a
        @click="showMobileMenu = !showMobileMenu"
        class="navbar-burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbar-menu"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div
      id="navbar-menu"
      class="navbar-menu"
      :class="{ 'is-active': showMobileMenu }"
    >
      <div class="navbar-end">
        <router-link to="/summer" class="navbar-item">Summer</router-link>
        <router-link to="/winter" class="navbar-item">Winter</router-link>

        <div class="navbar-item">
          <div class="buttons">
            <router-link to="/log-in" class="button is-light"
              >Log in</router-link
            >

            <router-link to="/cart" class="button is-success">
              <span class="icon"><i class="fas fa-shopping-cart"></i></span>
              <span>Cart</span>
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      showMobileMenu: false,
    };
  },
};
</script>

<style></style>
