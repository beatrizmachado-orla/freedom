<template>
  <div class="container">
    <div class="row align-items-center">
      <!-- Coluna do vídeo -->
      <div class="col-9 video-container">
        <video width="100%" ref="videoPlayer" autoplay loop style="border-radius: 18px;">
          <source :src="selectedVideo" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </div>

      <!-- Coluna das imagens clicáveis com títulos e descrições -->
      <div class="col-3 images-container">
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
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          src:"/src/assets/images/centralizacaodeias.png",
          title: "Centralização de IAs",
          description: "",
          videoSrc: "/src/assets/videos/ia.mp4"
        },
        {
          src: "/src/assets/images/humanodigital.png",
          title: "Humano digital",
          description: "",
          videoSrc: "/src/assets/videos/ia2.mp4"
        },
        {
          src: "/src/assets/images/Prompts.png",
          title: "Prompts",
          description: "",
          videoSrc: "/src/assets/videos/ia.mp4"
        }
      ],
      selectedVideo: "/src/assets/videos/ia.mp4", // vídeo inicial
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

.video-container {
  padding: 10px;
}

.images-container {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  border-radius: 20px;
  background:#FFFFFF0A;
  border: 1px solid #3F3F3F;
  padding: 20px;
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
