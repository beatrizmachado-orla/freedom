<template>
  <div class="container-fluid mb-5">
    <h2 class="section-title mb-5">Empresas que já usam IA</h2>
    <div class="carousel">
      <div class="carousel-track">
        <div v-for="(empresa, index) in empresas" :key="index" class="empresa-card">
          <img :src="empresa.src" class="image" :alt="empresa.title" />
        </div>
        <div v-for="(empresa, index) in empresas" :key="'repeat-' + index" class="empresa-card">
          <img :src="empresa.src" class="image" :alt="empresa.title" />
        </div>
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
          src: ".../assets/images/itauLogo.png",
          title: "Itau",
        },
        {
          src: ".../assets/images/claroLogo.png",
          title: "Claro",
        },
        {
          src: ".../assets/images/globoLogo.png",
          title: "Globo",
        },
        {
          src: ".../assets/images/nubankLogo.png",
          title: "Nubank",
        },
        {
          src: ".../assets/images/sabespLogo.png",
          title: "Sabesp",
        },
        {
          src: ".../assets/images/unimedLogo.png",
          title: "Unimed",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Contêiner do carrossel */
.carousel {
  overflow: hidden;
  width: 100%;
  height: 100px;
  margin: 70px auto;
  justify-items: center;
  align-items: center;
  align-content: center;
}

/* Faixa que contém as logos */
.carousel-track {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: calc(200%); /* Dobrar o tamanho para incluir as logos duplicadas */
  animation: scroll 100s linear infinite; /* Animação contínua */
}

.empresa-card {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 150px; /* Tamanho de cada logo */
}

.image {
  width: 90px;
  opacity: 0.8;
  transition: transform 0.3s ease-in-out;
}

.image:hover {
  transform: scale(1.1); /* Efeito de zoom ao passar o mouse */
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

.section-title {
  color: #ffc107;
  font-size: 1.5rem;
  text-align: center;
  margin-bottom: 20px;
}
</style>
