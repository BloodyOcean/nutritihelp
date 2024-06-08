<script setup>
  import { ref } from 'vue'
  import Navbar from './components/Navbar.vue'
</script>

<template>
  <div id="app">
    <header class="sticky top-0 z-50">
      <Navbar/>
    </header>

      <router-view></router-view>

      <footer></footer>

  </div>
</template>