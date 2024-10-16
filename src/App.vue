<script setup>
import HeaderLP from './components/HeaderLP.vue'
import HeroLP from './components/HeroLP.vue'
import Video from './components/Video.vue'
import Products from './components/Products.vue';
import FooterLP from './components/FooterLP.vue';
import Slider from './components/Slider.vue';
import Empresas from './components/Empresas.vue';
</script>

<template>
  <HeaderLP/>
  <HeroLP />
  <div class="info">
    <Video/>
    <Empresas/>
    <Products/>
    <Slider/>
  </div>
  <FooterLP/>
</template>

<style scoped>
.info {
  background-image: url("../src/assets/images/background.png");
  background-position: top right;
  background-repeat: no-repeat;
  background-size: cover;
  align-items: center;
  justify-content: center;
  display: flex;
  flex-direction: column;
  padding: 3rem;
}
.navbar-nav .nav-link:hover {
  color: #ffffff !important;
}
</style>