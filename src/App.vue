<script setup>
import { RouterLink, RouterView } from 'vue-router'

import navbar from './components/navbar.vue'
</script>

<template>
    <navbar/>
  <div class="app">
  <listeLivre/>
  <RouterView />
  </div>

 
</template>

<style scoped>
.app{
  background-image: url(/Gestion-bibliotheque/src/assets/images/fond.avif);
}
</style>