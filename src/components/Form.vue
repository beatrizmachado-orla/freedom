<template>
  <div class="form-container">
    <div class="row">
        <div class="form-title col-12 text-center">Solicite sua demonstração 100% gratuita.</div>
      </div>
    <div class="row">
      <!-- Logo -->
      <div class="col-6 d-flex align-items-center justify-content-center">
        <img src="../assets/images/logo.png" alt="Logo" class="img-fluid" />
      </div>

      <!-- Formulário de Solicitação -->
      <div class="col-6">
        <form @submit.prevent="submitForm">
          <div class="mb-3">
            <label for="nome" class="form-label">Nome completo</label>
            <input
              type="text"
              class="form-control"
              id="nome"
              v-model="formData.nome"
              required
            />
          </div>

          <div class="mb-3">
            <label for="empresa" class="form-label">Nome da empresa</label>
            <input
              type="empresa"
              class="form-control"
              id="empresa"
              v-model="formData.empresa"
              required
            />
          </div>

          <div class="mb-3">
            <label for="email" class="form-label">Email</label>
            <input
              type="email"
              class="form-control"
              id="email"
              v-model="formData.email"
              required
            />
          </div>

          <div class="mb-3">
            <label for="telefone" class="form-label">Telefone</label>
            <input
              type="telefone"
              class="form-control"
              id="telefone"
              v-model="formData.telefone"
              required
            />
          </div>
          <div class="btn-container">
              <button type="submit" class="btn">
                <span class="btn-text">Solicitar Agora</span>
              </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        nome: "",
        empresa: "",
        email: "",
        telefone: "",
      },
    };
  },
  methods: {
    submitForm() {
      // Aqui você pode lidar com o envio do formulário, como enviar os dados para uma API
      console.log("Dados do formulário:", this.formData);
      // Limpar o formulário após o envio (opcional)
      this.formData = {
        nome: "",
        empresa: "",
        email: "",
        telefone: "",
      };
    },
  },
};
</script>

<style scoped>
.form-container {
  background-image: url(..\assets\images\bg\persons.png);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: top;
  width: 100vw;
  height: 150vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.form-title {
  font-size: 24px;
  font-weight: 600;
  line-height: 31.2px;
  text-align: center;    
  color:#F7D11D;
  margin-bottom: 74px;
}

.form-label {
  font-family: 'Open Sans';
  font-size: 18px;
  line-height: 24px;
  text-align: left;
  color: #fff;
}

.form-control {
  width: Fill(530px);
  height: Fixed(65px);
  padding: 20px;
  border-radius: 6px;
  border: 2.42px solid #545252;
  background: linear-gradient(104.46deg, rgba(255, 255, 255, 0.06) 2.82%, rgba(173, 173, 173, 0.018) 102.97%);
  backdrop-filter: blur(2px);
  color: #fff;
}
.btn {
  width: 220px;
  height: 40px;
  padding: 12px;
  border-radius: 24px;
  background-color: #F7D11D;
  display: flex;
  align-items: center;
  justify-content: center;
}
.btn-text {
  font-family: Open Sans;
  font-size: 18px;
  font-weight: 600;
  line-height: 23.4px;
  text-align: left;
  color: #000000;
}
.btn-container{
  display: flex;
  justify-content: right;
  margin: 48px 0px;
}
</style>