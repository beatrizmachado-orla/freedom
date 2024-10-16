<template>
  <div id="products" class="container">
    <h2 class="section-title mb-5">Produtos da <span style="color:#fff">Freedom</span></h2>

    <div class="vantagem" v-for="(produto, index) in produtos" :key="index">
      <div :class="['vantagens', index % 2 === 0 ? 'normal-order' : 'reversed-order']">
        <div class="col-md-7">
          <img :src="produto.src" class="vantagem-image rounded-start" :alt="produto.title">
        </div>
        <div class="vantagem-box col-md-4" :style="index % 2 === 0 ? 'margin-left: 70px' : 'margin-right: 70px'">
          <div class="vantagem-card">
            <img class="check-icon" src="/src/assets/icons/check.png">
            <div class="vantagem-body">
              <h5 class="vantagem-title">{{ produto.Vantagem1 }}</h5>
            </div>
          </div>
          <div class="vantagem-card">
            <img class="check-icon" src="/src/assets/icons/check.png">
            <div class="vantagem-body">
              <h5 class="vantagem-title">{{ produto.Vantagem2 }}</h5>
            </div>
          </div>
          <div class="vantagem-card">
            <img class="check-icon" src="/src/assets/icons/check.png">
            <div class="vantagem-body">
              <h5 class="vantagem-title">{{ produto.Vantagem3 }}</h5>
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
      produtos: [
        {
          src:"../src/assets/images/humanodigital.png",
          title: "Humanos Digitais",
          Vantagem1: "Defina gênero, etnia e características para refletir sua identidade.",
          Vantagem2: "Escolha roupas, voz e expressões que representem a personalidade.",
          Vantagem3: "Determine a missão do avatar e crie diálogos que se adequem a seu público.",
        },
        {
          src: "../src/assets/images/centralizacaodeias.png",
          title: "Centralização de IAs",
          Vantagem1: "Crie conteúdos, imagens e faça pesquisas através de ferramentas unificadas.",
          Vantagem2: "Escolha roupas, voz e expressões que representem a personalidade.",
          Vantagem3: "Deixe seu trabalho automatizado por múltiplas IAs tornando o fluxo eficiente.",
        },
        {
          src: "../src/assets/images/Prompts.png",
          title: "Promps de Produtividade",
          Vantagem1: "Escolha um tema para gerar o conteúdo desejado.",
          Vantagem2: "Conteúdos para artigos, educação, saúde, marketing e muito mais.",
          Vantagem3: "Salve e organize os melhores prompts para usar quando quiser.",

        }
      ],
    };
  }
}
</script>

<style scoped>
.vantagem{
  display: flex;
  justify-content: space-between;
  color: #fff;
  margin: 70px 0px;
}
.vantagens {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  margin: 0 auto;
}
.normal-order {
  flex-direction: row; /* Ordem padrão: imagem -> vantagens */
}

.reversed-order {
  flex-direction: row-reverse; /* Inverte a ordem: vantagens -> imagem */
}

.check-icon {
  width: 24px;
  height: 24px;
  margin: 0px 5px;
}
.vantagem-box{
  display: flex;
  flex-direction: column;
  justify-content: space-around;  
}
.vantagem-card {
  width: 100%;
  border-radius: 10px;
  padding: 15px;
  margin: 22px 0px;
  display: flex;
  flex-direction: row;
  background:#FFFFFF0A;
  border: 1px solid #3F3F3F;
  backdrop-filter: blur(2px);
}

.vantagem-body {
  font-size: 18px;
}

.vantagem-title {
  font-family: Open Sans;
  font-size: 18px;
  font-weight: 400;
  line-height: 23.4px;
  text-align: left;

}

.vantagem-image {
  width: 100%;
}
.section-title {
  color: #ffc107;
  font-size: 1.5rem;
  text-align: center;
}
</style>