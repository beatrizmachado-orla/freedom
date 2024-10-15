<script setup>
import HeaderLP from './components/HeaderLP.vue'
import HeroLP from './components/HeroLP.vue'
import Video from './components/Video.vue'
import Products from './components/Products.vue';
import FooterLP from './components/FooterLP.vue';
</script>

<template>
  <HeaderLP msg="Primeira Configuração" />
  <HeroLP />
  <div class="info">
    <Video/>
    <Products/>
  </div>
  <FooterLP/>
</template>

<style scoped>
.info {
  background-image: url("../src/assets/images/background.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-color: rgba(51, 54, 2, 0.219);
}
.navbar-nav .nav-link:hover {
  color: #ffffff !important;
}
</style>