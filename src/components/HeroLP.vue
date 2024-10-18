<template>
  <main class="container-md herolp">
    <div class="row">
      <div class="col-lg-12 align-self-left">
        <img src="../assets/images/logo.png" alt="Logo" height="100vw" class="d-inline-block align-text-top mb-3">
        <p class="lead mb-4 text-white text-hero mb-5">
          Inteligência Artificial acessível para revolucionar sua <span style="color:#ffc107">criatividade</span> e <span style="color:#ffc107">produtividade</span>
        </p>
        <p class="h3 text-white mb-4">
          Solicite seu Protótipo 100% Gratuito
        </p>
        <button @click="solicitarPrototipo" class="btn btn-warning btn-lg">
          Solicitar agora
        </button>
      </div>
    </div>
  </main>
</template>

<script setup>

const solicitarPrototipo = () => {
  console.log('Solicitação de protótipo')
}
</script>

<style scoped>
.text-hero {
  font-size: 1rem;
}
.herolp {
  background-image: url(../assets/images/ai-face.png);
  background-repeat: no-repeat;
  background-size: contain;
  background-position: calc(100% + 50px) center;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: start;
  padding: 3rem;
}
.btn-warning:hover {
  background-color: #e0a800;
}
</style>