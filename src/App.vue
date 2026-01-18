<script setup>
  import { RouterView } from 'vue-router'
  import HeaderItem from './components/HeaderItem.vue'
  import FooterItem from './components/FooterItem.vue';
</script>

<template>
  <header-item></header-item>

  <RouterView />

  <footer-item></footer-item>
</template>

<style scoped>

</style>
