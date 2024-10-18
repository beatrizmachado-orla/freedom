<template>
  <div class="container-fluid">
    <div class="row align-items-center">
      <div class="text-video">
        <p class="title">Como nossos produtos funcionam?</p>
        <p class="subtitle">Veja aqui, na prática, como é rápido e fácil explorar nossos produtos.</p>
      </div>
      <div class="row justify-content-center">
        <div class="col-7 video-container">
          <video width="100%" ref="videoPlayer" autoplay loop>
            <source :src="selectedVideo" type="video/mp4" />
            Your browser does not support the video tag.
          </video>
        </div>
        <div class="col-2 images-container">
          <div
            v-for="(image, index) in images"
            :key="index"
            class="image-card"
            @click="selectVideo(index)"
            :class="{ 'active-image': selectedImage === index }"
          >
            <img
              :src="image.src"
              class="image"
            />
            <div class="image-overlay">
              <h3 class="image-title">{{ image.title }}</h3>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          src:"../src/assets/images/centralizacaodeias.png",
          title: "Centralização de IAs",
          description: "",
          videoSrc: "../src/assets/videos/ia.mp4"
        },
        {
          src: "../src/assets/images/humanodigital.png",
          title: "Humano digital",
          description: "",
          videoSrc: "../src/assets/videos/ia2.mp4"
        },
        {
          src: "../src/assets/images/Prompts.png",
          title: "Prompts",
          description: "",
          videoSrc: "../src/assets/videos/ia.mp4"
        }
      ],
      selectedVideo: "../src/assets/videos/ia.mp4", // vídeo inicial
      selectedImage: 0 // imagem inicial selecionada
    };
  },
  methods: {
    selectVideo(index) {
      this.selectedImage = index;
      this.selectedVideo = this.images[index].videoSrc;
      this.$refs.videoPlayer.load();
    }
  }
};
</script>

<style scoped>

.video-container video {
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
}
.title{
  font-family: Open Sans;
  font-size: 24px;
  font-weight: 600;
  line-height: 31.2px;
  text-align: center;
  color: #ffc107;
  margin-bottom: 16px;
}
.subtitle{
  font-family: Open Sans;
  font-size: 18px;
  font-weight: 600;
  line-height: 21.6px;
  text-align: center;
  color: #fff;
}
.images-container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background:#FFFFFF0A;
  border: 1px solid #3F3F3F;
  backdrop-filter: blur(2px);
  border-radius: 20px;
  padding: 10px;
  margin: 30px 0;
}
.image-card {
  position: relative;
  margin: 15px;
  cursor: pointer;
}
.image-title{
  font-size: 1.2rem;
}

.image-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.295); /* Fundo escuro com opacidade */
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
}

.image-card:hover{
  transition: all 0.5s ease-in-out;
  transform: scale(1.1);
}

.image {
  width: 100%;
  border-radius: 10px;
}

.image.active-image {
  transform: scale(1.1);
}

h3, p {
  margin: 0;
  text-align: center;
}
</style>
