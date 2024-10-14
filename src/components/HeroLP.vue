<template>
  <main class="container herolp">
    <div class="row">
      <div class="col-lg-12 align-self-left">
        <img src="../assets/images/logo.png" alt="Logo" height="123" class="d-inline-block align-text-top mb-3">
        <p class="lead mb-4 text-white text-hero">
          Inteligência Artificial acessível para revolucionar sua <span style="color:#ffc107">criatividade</span> e <span style="color:#ffc107">produtividade</span>
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
  font-family: 'Raleway', sans-serif;
}
.herolp{
  width: 100vw;
  background-image: url(../assets/images/ai-face.png);
  background-repeat: no-repeat;
  background-size: contain;
  background-position: top right;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: start;
}
.navbar-nav .nav-link {
  transition: color 0.3s ease;
}

.navbar-nav .nav-link:hover {
  color: #ffc107 !important;
}

.btn-warning:hover {
  background-color: #e0a800;
}
</style>