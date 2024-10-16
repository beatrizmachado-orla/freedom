<template>
  <div id="products" class="container">
    <h2 class="section-title mb-5">Produtos da <span style="color:#fff">Freedom</span></h2>

    <!-- Humanos Digitais -->
    <div class="mb-5 text-white" v-for="(produto, index) in produtos" :key="index">
      <div class="vantagens">
        <div class="col-md-7">
          <img :src="produto.src" class="vantagem-image rounded-start" alt="Humanos Digitais">
        </div>
        <div class="col-md-5">
          <div class="vantagem-card">
            <img class="check-icon" src="/src/assets/icons/check.png">
            <div class="vantvantagem-body">
              <h5 class="vantvantagem-title">{{produto.Vantagem1}}</h5>
            </div>
          </div>
          <div class="vantagem-card">
            <img class="check-icon" src="/src/assets/icons/check.png">
            <div class="vantvantagem-body">
              <h5 class="vantvantagem-title">{{produto.Vantagem2}}</h5>
            </div>
          </div>
          <div class="vantagem-card">
            <img class="check-icon" src="/src/assets/icons/check.png">
            <div class="vantvantagem-body">
              <h5 class="vantvantagem-title">{{produto.Vantagem3}}</h5>
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
          src:"/src/assets/images/centralizacaodeias.png",
          title: "Humanos Digitais",
          Vantagem1: "Defina gênero, etnia e características para refletir sua identidade.",
          Vantagem2: "Escolha roupas, voz e expressões que representem a personalidade.",
          Vantagem3: "Determine a missão do avatar e crie diálogos que se adequem a seu público.",
        },
        {
          src: "/src/assets/images/humanodigital.png",
          title: "Centralização de IAs",
          Vantagem1: "Crie conteúdos, imagens e faça pesquisas através de ferramentas unificadas.",
          Vantagem2: "Escolha roupas, voz e expressões que representem a personalidade.",
          Vantagem3: "Deixe seu trabalho automatizado por múltiplas IAs tornando o fluxo eficiente.",
        },
        {
          src: "/src/assets/images/Prompts.png",
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
.section-title {
  color: #ffc107;
  font-size: 1.5rem;
  font-weight: bold;
  text-align: center;
}
.check-icon {
  width: 40px;
  height: 40px;
  margin: 10px;
}
.vantagens{
  display: flex;
  justify-content: center;
  align-items: center;
}
.vantagem-card {
  border-radius: 10px;
  padding: 10px;
  margin: 32px 0px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  background:#FFFFFF0A;
  border: 1px solid #3F3F3F;
}
.vantagem-body{
  font-size: 18px;
}
.vantagem-title {
  color: #fff;
  font-size: 1.5rem;
  font-weight: bold;
}
.vantagem-image{
  width: 100%;
  padding: 20px;
}

</style>