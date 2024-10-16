<template>
    <div id="about" >
      <div class="text-video">
        <p class="h1 text-warning title">O que é a <span class="text-white">Freedom</span>?</p>
        <p class="text-white h6 subtitle font-weight-light mb-5">A Freedom é uma empresa de inteligência artificial focada em democratizar o acesso à IA, oferecendo soluções para criatividade e produtividade. Lideramos a transformação para que empresas e profissionais tenham acesso fácil e personalizado às melhores soluções de IA.</p>
      </div>
      <video width="100%" ref="videoPlayer" controls style="border-radius: 18px;">
        <source src="../src/assets/images/ia.mp4" type="video/mp4" />
        Your browser does not support the video tag.
      </video>
    </div>
</template>

<script setup>

const solicitarPrototipo = () => {
  console.log('Solicitação de protótipo')
}
</script>

<style scoped>
.text-video {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 0 15%;
}
#about {
  margin: 0px 1vw 140px 1vw;
  background:#FFFFFF0A;
  border: 1px solid #3F3F3F;
  backdrop-filter: blur(2px);
  border-radius: 50px;
  padding: 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.title{
  font-size: 56px;
}
.subtitle{
  font-family: Raleway;
  font-size: 18px;
  font-weight: 500;
  line-height: 25.2px;
  text-align: center;
}
</style>