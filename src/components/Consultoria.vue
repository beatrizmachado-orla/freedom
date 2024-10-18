<template>
  <div class="container-fluid">
    <div class="section-consultoria col text-white">
        <p class="title-section">Consultoria personalizada</p>
        <p class="subtitle-section">Empresas que adotam tecnologias avançadas não apenas se destacam, mas também lideram o mercado. A inteligência artificial é a chave para otimizar processos, aumentar a eficiência e impulsionar a inovação. A Freedom está aqui para ajudar a impulsionar a sua empresa a transformar desafios em oportunidades através de uma consultoria personalizada.</p>
      </div>
      <div class="row">
        <div class="col card text-white" v-for="(card, index) in cards" :key="index">
          <img :src="card.img" alt="" srcset="">
          <div class="title">{{card.title}}</div>
          <div class="description">{{card.description}}</div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          img: "src/assets/images/postit.png",
          title: "Avaliação",
          description: "Entendemos as necessidades do seu negócio e identificamos as informações em que a IA pode trazer o maior impacto.",
        },
        {
          img: "src/assets/images/solucoespersonalizadas.png",
          title: "Soluções Personalizadas",
          description: "Criamos soluções sob medida para sua empresa, ajudando na escolha das ferramentas de IA mais adequadas.",
        },
        {
          img: "src/assets/images/treinamento.png",
          title: "Treinamento",
          description: "Ensinar sua equipe a usar as novas ferramentas de maneira eficaz, e aproveitar ao máximo os recursos oferecidos pela IA.",
        },
        {
          img: "src/assets/images/suporte.png",
          title: "Suporte Contínuo",
          description: "Acompanhamos de perto a implementação e oferecemos suporte contínuo para com o melhor da tecnologia em seu negócio.",
        },
      ],
    }
  }
}
</script>

<style>
.container-fluid{
  padding: 0 5vw !important;
}
.section-consultoria{
  margin: 40px;
}
.card{
  background:#FFFFFF0A !important;
  border: 1px solid #3F3F3F !important;
  backdrop-filter: blur(2px);
  border-radius: 20px !important;
  padding: 15px !important;
  margin: 9px !important;
  gap: 10px;
}
.title{
  font-family: Open Sans;
  font-size: 21.55px;
  font-weight: 600;
  line-height: 28.01px;
  text-align: left;
}
.description{
  font-family: Open Sans;
  font-size: 16.16px;
  font-weight: 400;
  line-height: 21.01px;
  text-align: left;
}
.title-section{
  color: #fbd016;
  font-family: Open Sans;
  font-size: 60px;
  font-weight: 600;
  line-height: 80px;
  text-align: center;
}
.subtitle-section{
  font-family: Open Sans;
  font-size: 19.85px;
  font-weight: 400;
  line-height: 25.8px;
  text-align: center;
}
</style>