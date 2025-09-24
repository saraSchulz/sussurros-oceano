<script setup>
import headerComponent from '@/components/headerComponent.vue';
import footerComponent from './components/footerComponent.vue';
import BannerHomeComponent from './components/home/bannerHomeComponent.vue'
import selectHomeComponent from './components/home/selectHomeComponent.vue';
import sobreComponent from './components/home/sobreComponent.vue';
import maisSobreComponent from './components/home/maisSobreComponent.vue';
</script>

<template>
  <header>
    <headerComponent />
  </header>
  <main>
    <BannerHomeComponent />
    <selectHomeComponent />
    <sobreComponent />
    mai
    <maisSobreComponent />
  </main>
  <footer>
    <footerComponent />
  </footer>
</template>

<style scoped>

</style>
