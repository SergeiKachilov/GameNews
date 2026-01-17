<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HeaderItem from './components/HeaderItem.vue'
import FooterItem from './components/FooterItem.vue';
</script>

<template>
    <HeaderItem/>

      <!-- <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav> -->

  <RouterView />

  <footer-item></footer-item>
</template>

<style scoped>

</style>
