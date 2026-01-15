<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HeaderItem from './components/HeaderItem.vue'
</script>

<template>
    <HeaderItem/>

      <!-- <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav> -->

  <RouterView />
</template>

<style scoped>

</style>
