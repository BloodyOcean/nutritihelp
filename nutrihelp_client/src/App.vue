<script setup>
import { ref } from 'vue'
import Navbar from './components/Navbar.vue'

</script>

<template>
  <div id="app">
    <header>
      <Navbar />
    </header>

    <router-view class="mt-2 p-5 relative"></router-view> 

    <footer></footer>

  </div>
</template>