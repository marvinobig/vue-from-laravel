<script setup>
import NavBar from './components/NavBar.vue';
</script>

<template>
  <header class="sticky top-0 p-3">
    <NavBar />
  </header>

  <RouterView />
</template>