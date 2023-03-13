<script setup>
import { RouterLink, RouterView } from 'vue-router'
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
        <li><RouterLink class="text_deco_none" to="/">Log-In</RouterLink></li>
        <li><RouterLink class="text_deco_none" to="/about">Register</RouterLink></li>
      </ul>
    </div>
  </header>
  <div class="info_body">
    <div class="product_menu">
      <ul>
        <div class="list_category"> 
          <li class="bald_menu_item">MEN</li>
          <ul class="sub_category_list">
            <li>SUITS</li>
            <li>OUTERWEAR</li>
            <li>SHIRTS</li>
            <li>BLAZERS</li>
            <li>POLOS & T-SHIRTS</li>
            <li>PANTS</li>
          </ul>
        </div>
        <div class="list_category"> 
          <li class="bald_menu_item">WOMEN</li>
          <ul class="sub_category_list">
            <li>SUITS</li>
            <li>OUTERWEAR</li>
            <li>SHIRTS</li>
            <li>BLAZERS</li>
            <li>POLOS & T-SHIRTS</li>
            <li>PANTS</li>
          </ul>
        </div>
      </ul>
    </div>
    <RouterView />
  </div>
</template>
