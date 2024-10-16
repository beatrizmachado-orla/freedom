<template>
<div class="container p-3 mb-5">
  <div class="box-productivity">
    <div class="card-productivity" v-for="(beneficio, index) in beneficios" :key="index">
      <div class="title">{{ beneficio.title }}</div>
      <div class="percentual">{{ beneficio.Percentual }}</div>
      <div class="description">{{ beneficio.Descricão }}</div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  data() {
    return {
      beneficios: [
        {
          title: "Economize até",
          Percentual: "50%",
          Descricão: "dos gastos usando as principais ferramentas de IA.",
        },
        {
          title: "Reduza até",
          Percentual: "60%",
          Descricão: "de tempo em produção de vídeos e conteúdos visuais.",
        },
        {
          title: "Aumente até",
          Percentual: "40%",
          Descricão: "a produtividade e eficiência com ferramentas centralizadas.",
        },
        {
          title: "Garanta até",
          Percentual: "30%",
          Descricão: "mais de consistência na qualidade dos conteúdos.",
        },
      ],
    };
  }
}
</script>

<style scoped>
.box-productivity{
  display: flex;
}
.card-productivity{
  width: 100%;
  background:#FFFFFF0A;
  border: 1px solid #3F3F3F;
  backdrop-filter: blur(2px);
  width: Fixed (310px)px;
  height: Fixed (244px)px;
  padding: 36px 15px 36px 15px;
  gap: 10px;
  border-radius: 20px;
  margin: 10px;
}
.title{
  color: #fad019;
  font-family: Open Sans;
  font-size: 24px;
  font-weight: 600;
  line-height: 31.2px;
  text-align: center;
}
.percentual{
  color: #fff;
  font-family: Open Sans;
  font-size: 56px;
  font-weight: 600;
  line-height: 72.8px;
  text-align: center;
}
.description{
  color: #fff;
  font-family: Open Sans;
  font-size: 18px;
  font-weight: 400;
  line-height: 23.4px;
  text-align: center;
}
</style>