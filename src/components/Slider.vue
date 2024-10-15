<template>
  <div class="slider-container">
    <!-- Seção de vídeo -->
    <div class="video-section">
      <video autoplay loop muted>
        <source src="../assets/images/ia.mp4" type="video/mp4" />
        Seu navegador não suporta o vídeo.
      </video>
    </div>

    <!-- Seção de slides -->
    <div class="slides-section">
      <div class="d-flex flex-column justify-content-between">
        <div class="slide-item" v-for="(slide, index) in slides" :key="index">
          <h3>{{ slide.title }}</h3>
          <p>{{ slide.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      slides: [
        { title: "Centralização de IAs", description: "Claude, Bing, ChatGPT" },
        { title: "Humano Digital", description: "Os melhores Prompts disponíveis" },
        { title: "Prompts", description: "Os melhores Prompts disponíveis" }
      ]
    };
  },
};
</script>

<style scoped>
.slider-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #0d0d0d;
  padding: 20px;
  border-radius: 10px;
}

.video-section {
  flex: 3;
  margin-right: 20px;
}

.video-section video {
  width: 100%;
  border-radius: 10px;
}

.slides-section {
  flex: 1;
  position: relative;
  overflow: hidden;
}

.slide-wrapper {
  display: flex;
  transition: transform 0.3s ease;
  width: 300%;
}

.slide-item {
  flex: 1;
  padding: 20px;
  background-color: #212121;
  color: #fff;
  text-align: center;
  border-radius: 10px;
  justify-content: space-between;
  margin: 20px 0px;
}

.controls {
  display: flex;
  justify-content: space-between;
  margin-top: 10px;
}

button {
  background-color: #f0ad4e;
  color: white;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 5px;
}

button:disabled {
  background-color: #ddd;
  cursor: not-allowed;
}
</style>
