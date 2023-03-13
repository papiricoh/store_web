<script setup>
import { RouterLink, RouterView } from 'vue-router'
import ProductMenu from './components/ProductMenu.vue';
</script>

<template>
  <header>
    <div id="main_header">
      <ul class="horizontal_menu">
        <li><RouterLink class="text_deco_none" to="/">Home</RouterLink></li>
        <li><RouterLink class="text_deco_none" to="/about">About</RouterLink></li>
      </ul>
      <img height="140" src="https://dieselpunkcore.com/wp-content/uploads/2014/06/logo-placeholder.png" alt="logo">
      <ul class="horizontal_menu">
        <li><RouterLink class="text_deco_none" to="/log-in">Log-In</RouterLink></li>
        <li><RouterLink class="text_deco_none" to="/about">Register</RouterLink></li>
      </ul>
    </div>
  </header>
  <div class="info_body">
    <div class="product_menu">
      <ProductMenu />
    </div>
    <RouterView />
  </div>
</template>
