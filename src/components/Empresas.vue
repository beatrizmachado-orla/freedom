<template>
  <div class="container mb-5">
    <h2 class="section-title mb-5">Empresas que já usam IA</h2>
    <div class="empresas-box">
        <div v-for="empresa in empresas" :key="index" class="empresa-card" >
          <img :src="empresa.src" class="image"/>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      empresas: [
        {
          src:"src/assets/images/itauLogo.png",
          title: "Itau",
        },
        {
          src: "src/assets/images/claroLogo.png",
          title: "Claro",
        },
        {
          src: "src/assets/images/globoLogo.png",
          title: "Globo",
        },
        {
          src: "src/assets/images/nubankLogo.png",
          title: "Nubank",
        },
        {
          src: "src/assets/images/sabespLogo.png",
          title: "Sabesp",
        },
        {
          src: "src/assets/images/unimedLogo.png",
          title: "Unimed",
        }
      ],
    };
  }
};
</script>

<style scoped>
.empresas-box{
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 50px;
  margin: 50px;
}
.section-title {
  color: #ffc107;
  font-size: 1.5rem;
  text-align: center;
}
</style>