<template>
  <div class="text-white bg-transparent py-4 fixed-top bg-gradient">
    <nav class="navbar navbar-expand-lg navbar-dark bg-transparent">
      <div class="container">
        <router-link class="navbar-brand fs-4 fw-bold" to="/">
          <img src="../assets/images/logo.png" alt="Logo" height="24" class="d-inline-block align-text-top">
        </router-link>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link text-warning" href="#about">Sobre nós</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-warning" href="#services">Serviços</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-warning" href="#benefits">Benefícios</a>            
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script setup>

</script>

<style scoped>
.bg-gradient {
  backdrop-filter: blur(2px);
  background: linear-gradient(180deg, rgba(179, 179, 179, 0.54) 0%, rgba(39, 39, 39, 0.45) 73.4%, rgba(0, 0, 0, 0.09) 100%),
linear-gradient(0deg, rgba(41, 41, 41, 0.17), rgba(41, 41, 41, 0.17)) !important;

}
.navbar-nav .nav-link {
  transition: color 0.3s ease;
  font-size: 20px;
  margin: 0px 10px;
}

.navbar-nav .nav-link:hover {
  color: #ffc107 !important;
}

.btn-warning:hover {
  background-color: #e0a800;
}
</style>