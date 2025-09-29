<script setup>
import { ref, onMounted } from 'vue'
import Navbar from './component/Navbar.vue';
</script>

<template>
  <div>
    <Navbar />
    <router-view />
  </div>
</template>



<style scoped>

</style>
