<template>
  <div class="container">
    <div class="accordion custom-accordion" id="accordionExample">
      <div class="accordion-item" v-for="(faq, index) in faqs" :key="index">
        <h2 class="accordion-header d-flex justify-content-between align-items-center">
          <span class="accordion-title">{{ faq.pergunta }}</span>
          <button class="accordion-button collapsed custom-button" type="button" 
            data-bs-toggle="collapse" 
            :data-bs-target="'#collapse' + index" 
            :aria-controls="'collapse' + index">
          </button>
        </h2>
        <div :id="'collapse' + index" class="accordion-collapse collapse" 
          :aria-labelledby="'heading' + index" 
          data-bs-parent="#accordionExample">
          <div class="accordion-body custom-body">
            {{ faq.resposta }}
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
      faqs: [
        {
          pergunta: "Como posso integrar a IA na minha empresa?",
          resposta: "Integrar a inteligência artificial na sua empresa envolve uma série de etapas estratégicas, começando pela avaliação das necessidades e definição de objetivos claros. É essencial escolher a tecnologia adequada, considerando a escalabilidade e a integração com sistemas existentes. Desenvolver um plano de ação e capacitar a equipe por meio de treinamentos são fundamentais para garantir uma transição suave. Iniciar com um projeto piloto permite testar a solução e coletar feedback, seguido por monitoramento e ajustes contínuos. Após o sucesso inicial, a expansão da aplicação da IA para outras áreas e a atualização constante sobre novas tecnologias ajudarão a manter a competitividade no mercado."
        },
        {
          pergunta: "Quais são os benefícios da centralização de IAs?",
          resposta: "Integrar a inteligência artificial na sua empresa envolve uma série de etapas estratégicas, começando pela avaliação das necessidades e definição de objetivos claros. É essencial escolher a tecnologia adequada, considerando a escalabilidade e a integração com sistemas existentes. Desenvolver um plano de ação e capacitar a equipe por meio de treinamentos são fundamentais para garantir uma transição suave. Iniciar com um projeto piloto permite testar a solução e coletar feedback, seguido por monitoramento e ajustes contínuos. Após o sucesso inicial, a expansão da aplicação da IA para outras áreas e a atualização constante sobre novas tecnologias ajudarão a manter a competitividade no mercado."
        },
        {
          pergunta: "Como funciona a criação de prompts pré-definidos?",
          resposta: "Integrar a inteligência artificial na sua empresa envolve uma série de etapas estratégicas, começando pela avaliação das necessidades e definição de objetivos claros. É essencial escolher a tecnologia adequada, considerando a escalabilidade e a integração com sistemas existentes. Desenvolver um plano de ação e capacitar a equipe por meio de treinamentos são fundamentais para garantir uma transição suave. Iniciar com um projeto piloto permite testar a solução e coletar feedback, seguido por monitoramento e ajustes contínuos. Após o sucesso inicial, a expansão da aplicação da IA para outras áreas e a atualização constante sobre novas tecnologias ajudarão a manter a competitividade no mercado."
        },
        {
          pergunta: "Quais dados são coletados e como são protegidos?",
          resposta: "Integrar a inteligência artificial na sua empresa envolve uma série de etapas estratégicas, começando pela avaliação das necessidades e definição de objetivos claros. É essencial escolher a tecnologia adequada, considerando a escalabilidade e a integração com sistemas existentes. Desenvolver um plano de ação e capacitar a equipe por meio de treinamentos são fundamentais para garantir uma transição suave. Iniciar com um projeto piloto permite testar a solução e coletar feedback, seguido por monitoramento e ajustes contínuos. Após o sucesso inicial, a expansão da aplicação da IA para outras áreas e a atualização constante sobre novas tecnologias ajudarão a manter a competitividade no mercado."
        }
      ]
    };
  },
};
</script>

<style scoped>
/* Accordion escuro */
.custom-accordion .accordion-item {
  border: none;
  margin: 10px 0px;
  background: #FFFFFF14 !important;
  border: 1px solid #3F3F3F !important;
  backdrop-filter: blur(2px);
  border-radius: 30px !important;
  padding: 40px;
  transition: height 5s ease;
}

.custom-button {
  width: 30px;
  height: 30px;
  border-radius: 50% !important;
  background-color: #F7D11D;
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
}

.custom-accordion .accordion-button {
  padding: 20px !important;
}

.custom-accordion .accordion-header {
  display: flex; 
  justify-content: space-between;
  align-items: center;
}

.custom-accordion .accordion-button:focus {
  box-shadow: none;
}

.custom-body {
  color: #fff;
}
.accordion-title{
  font-family: Open Sans;
  font-size: 20px;
  font-weight: 700;
  line-height: 28px;
  text-align: left;
  color: #F7D11D;
}
</style>