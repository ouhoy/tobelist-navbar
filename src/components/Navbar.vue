<script setup lang="ts">
import {ref} from "vue";

const menu = ref(false);

function handleMenuClick() {
  menu.value = !menu.value;
}


</script>

<template>
  <div class="container navbar">
    <nav class="mobile-menu hide-for-tablet">
      <div class="nav-top">
        <div class="logo">
          <img src="src/assets/images/logo.svg" alt="tobelist.net logo">
          <h2 class="hide-for-mobile">tobelist.net</h2>
        </div>

        <p @click="handleMenuClick">{{menu? "Close": "Menu"}}</p>
      </div>
      <div v-if="menu">
        <ul class="links">
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Privacy</a></li>
          <li><a href="#">Blog</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
        <div class="cta">
          <div class="login"><a href="#">Login →</a></div>
          <button>Get started</button>

        </div>
      </div>

    </nav>

    <nav class="desktop-menu hide-for-md hide-for-mobile">
      <div class="logo">
        <img src="src/assets/images/logo.svg" alt="tobelist.net logo">
        <h2 class="hide-for-mobile">tobelist.net</h2>
      </div>

      <div class="menu-cta">
        <div class="links">
          <a href="#">Home</a>
          <a href="#">About</a>
          <a href="#">Privacy</a>
          <a href="#">Blog</a>
          <a href="#">Contact</a>
        </div>
        <div class="cta">
          <div class="login"><a href="#">Login</a></div>
          <button>Get started</button>
        </div>
      </div>
    </nav>
  </div>
</template>

<style lang="scss">

@import "src/styles/navbar.scss";

</style>