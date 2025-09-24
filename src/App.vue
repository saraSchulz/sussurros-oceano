<script setup>
import headerComponent from '@/components/HeaderComponent.vue';
import footerComponent from '@/components/FooterComponent.vue';
import bannerSobreNosComponent from './components/sobreNos/bannerSobreNosComponent.vue';
import nossoObjetivoComponent from './components/sobreNos/nossoObjetivoComponent.vue';
import nossaEquipeComponent from './components/sobreNos/nossaEquipeComponent.vue';
</script>

<template>
  <header>
    <headerComponent />
  </header>
  <main>
    <bannerSobreNosComponent/>
    <nossoObjetivoComponent/>
    <nossaEquipeComponent/>
  </main>
  <footer>
    <footerComponent />
  </footer>
</template>

<style scoped>

</style>
