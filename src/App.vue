<script setup>
import headerComponent from '@/components/headerComponent.vue';
import foooterComponent from './components/foooterComponent.vue';
import BannerHomeComponent from './components/home/bannerHomeComponent.vue'
</script>

<template>
  <header>
    <headerComponent />
  </header>
  <main>
    <BannerHomeComponent />
  </main>
  <footer>
    <foooterComponent />
  </footer>
</template>

<style scoped>

</style>
