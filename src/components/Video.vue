<template>
    <div id="about">
      <div class="text-video">
        <p class="h1 text-warning title">O que é a <span class="text-white">Freedom</span>?</p>
        <p class="text-white h6 subtitle">A Freedom é uma empresa de inteligência artificial focada em democratizar o acesso à IA, oferecendo soluções para criatividade e produtividade. Lideramos a transformação para que empresas e profissionais tenham acesso fácil e personalizado às melhores soluções de IA.</p>
      </div>
      <div class="embed-responsive embed-responsive-16by9">
        <iframe class="embed-responsive-item" height="700" width="1080" src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0" allowfullscreen></iframe>
      </div>
    </div>
</template>

<script setup>

const solicitarPrototipo = () => {
  console.log('Solicitação de protótipo')
}
</script>

<style scoped>
.text-video {
  width: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin-bottom: 30px;
}
#about {
  background-color: #000;
  border: 1px solid #FFFFFF4D;
  border-radius: 50px;
  margin: 10%;
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