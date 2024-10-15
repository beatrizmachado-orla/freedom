<template>
    <div id="about" >
      <div class="text-video">
        <p class="h1 text-warning title">O que é a <span class="text-white">Freedom</span>?</p>
        <p class="text-white h6 subtitle font-weight-light mb-5">A Freedom é uma empresa de inteligência artificial focada em democratizar o acesso à IA, oferecendo soluções para criatividade e produtividade. Lideramos a transformação para que empresas e profissionais tenham acesso fácil e personalizado às melhores soluções de IA.</p>
      </div>
        <iframe class="embed-responsive-item" height="600vw" width="100%" src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0" allowfullscreen></iframe>
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
  width: 80vw;
  margin: 80px 50px;
  background: linear-gradient(-90deg, rgba(255, 255, 255, 0.096) 0%, rgba(0,0,0,0) 100%);  border: 1px solid #3F3F3F;
  backdrop-filter: blur(2px);
  border: 1px solid #3F3F3F;
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