<script setup>
import HeaderLP from './components/HeaderLP.vue'
import HeroLP from './components/HeroLP.vue'
import Video from './components/Video.vue'
import Products from './components/Products.vue';
import FooterLP from './components/FooterLP.vue';
import Slider from './components/Slider.vue';
import Empresas from './components/Empresas.vue';
import Produtividade from './components/Produtividade.vue';
import Consultoria from './components/Consultoria.vue';
import Depoimentos from './components/Depoimentos.vue';
import Faq from './components/Faq.vue';
import testes from './components/testes.vue';
</script>

<template>
  <HeaderLP/>
  <HeroLP />
  <div class="info">
    <Video/>
    <Empresas/>
    <Products/>
    <Produtividade/>
    <Slider/>
    <Consultoria/>
    <Depoimentos/>
    <Faq/>
  </div>
  <FooterLP/>
</template>

<style scoped>
.info {
  background-image:
    url("./assets/images/bg/Gradiente.png"),
    url("./assets/images/bg/Verde.png"),
    url("./assets/images/bg/Amarelo.png");
  background-position: top;
  background-repeat: no-repeat;
  background-size: 100%;
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