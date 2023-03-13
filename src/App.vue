<script setup>
import { RouterLink, RouterView } from 'vue-router'
import ProductMenu from './components/ProductMenu.vue';
</script>

<script>
export default {
  data() {
    return {
      product_menu: true
    }
  },
}
</script>

<template>
  <header>
    <div id="main_header">
      <ul class="horizontal_menu">
        <li><RouterLink @click="product_menu = true" class="text_deco_none" to="/">Home</RouterLink></li>
        <li><RouterLink @click="product_menu = true" class="text_deco_none" to="/about">About</RouterLink></li>
      </ul>
      <RouterLink @click="product_menu = true" to="/" ><img height="140" src="/logo.jpeg" alt="logo"></RouterLink>
      <ul class="horizontal_menu">
        <li><RouterLink @click="product_menu = false" class="text_deco_none" to="/log-in">Log-In</RouterLink></li>
        <li><RouterLink @click="product_menu = false" class="text_deco_none" to="/register">Register</RouterLink></li>
      </ul>
    </div>
  </header>
  <div class="info_body">
    <div v-if="product_menu" class="product_menu">
      <ProductMenu />
    </div>
    <RouterView />
  </div>
</template>
