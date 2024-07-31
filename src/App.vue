<script>
  import { RouterLink, RouterView } from 'vue-router'
  import sidebar from './components/sidebar.vue';
  let showSideBar=true;

  
  
</script>

<template>
  <header class="top-bar spread">
    <nav class="top-bar-nav">
      <router-link to="/" class="top-bar-link">
        <i class="icofont-spoon-and-fork"></i>
        <span>Home</span>
      </router-link>
      <router-link to="/products" class="top-bar-link">
        <span>Products</span>
      </router-link>
      <router-link to="/past-orders" class="top-bar-link">
        <span>Past Orders</span>
      </router-link>
    </nav>
    <!-- <router-link @click="closeCart" class="top-bar-cart-link">
      <i class="icofont-cart-alt icofont-1x"></i>
      <span>Cart ({{totalQuantity}})</span>
    </router-link> -->
  </header>

  <RouterView />
  <sidebar
  v-show="showSideBar" :close="closeCart"
  :cart="cart"
  :inventory="inventory"
  :remove="removeItem"></sidebar>
</template>

<style scoped>
  
</style>
