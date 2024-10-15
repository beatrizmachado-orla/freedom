<template>
  <div id="products" class="container">
    <h2 class="section-title mb-5">Produtos da Freedom</h2>

    <!-- Humanos Digitais -->
    <div class="card mb-5 text-white">
      <div class="row g-0">
        <div class="col-md-6">
          <img src="../assets/images/woman.png" class="img-fluid rounded-start" alt="Humanos Digitais">
        </div>
        <div class="col-md-6 d-flex align-items-center">
          <div class="card-body">
            <h5 class="card-title">Humanos Digitais</h5>
            <p class="card-text">Soluções personalizadas de humanos digitais para vídeos e treinamentos.</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Centralização de IAs -->
    <div class="card mb-5 text-white">
      <div class="row g-0 flex-row-reverse">
        <div class="col-md-6">
          <img src="../assets/images/ias.png" class="img-fluid rounded-start" alt="Centralização de IAs">
        </div>
        <div class="col-md-6 d-flex align-items-center">
          <div class="card-body">
            <h5 class="card-title">Centralização de IAs</h5>
            <p class="card-text">Acesse e compare diferentes IAs, e use a Freedom para encontrar a solução mais adequada para suas necessidades.</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Prompts de Produtividade -->
    <div class="card mb-5 text-white">
      <div class="row g-0">
        <div class="col-md-6">
          <img src="../assets/images/bestPrompts.png" alt="" width="100%" height="100%" class="img-fluid rounded-start">
        </div>
        <div class="col-md-6 d-flex align-items-center">
          <div class="card-body">
            <h5 class="card-title">Prompts de Produtividade</h5>
            <p class="card-text">Acesse e compare diferentes IAs, e use a Freedom para encontrar a solução mais adequada para suas necessidades.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// No additional script setup needed for this component
</script>

<style scoped>
.section-title {
  color: #ffc107;
  font-size: 2rem;
  font-weight: bold;
}

.card {
  background: linear-gradient(-90deg, rgba(158, 157, 157, 0.144) 0%, rgba(0,0,0,0) 100%);
  border: 1px solid #3F3F3F;
  border-radius: 50px;
  backdrop-filter: blur(2px);
}

.card-title {
  color: #fff;
  font-size: 1.5rem;
  font-weight: bold;
}

</style>