<script setup>
import HeaderLP from './components/HeaderLP.vue'
import HeroLP from './components/HeroLP.vue'
import Video from './components/Video.vue'
import Products from './components/Products.vue';
</script>

<template>
  <HeaderLP msg="Primeira Configuração" />
  <HeroLP />
  <div class="info">
    <Video/>
    <Products/>
  </div>
</template>

<style scoped>
.info {
  background-image: url(../assets/images/ai-face.png);
  background-repeat: no-repeat;
  background-size: contain;
  background-position: top right;

}
</style>