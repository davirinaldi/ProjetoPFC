<template>
  <div class="container mt-5">
    <h1 class="login-title">PFC – Controle Financeiro Pessoal</h1> <div class="row"></div>
    <div class="row">
      <div class="col-md-8 offset-md-2">
        <div class="caixa-login">
          <div class="corpo-caixa-login">
            <form @submit.prevent="handleSubmit">
              <div class="grupo-formulario">
                <input
                  type="text"
                  class="campo-formulario"
                  id="username"
                  placeholder="Usuário"
                  v-model="nomeUsuario"
                  required
                />
              </div>
              <div class="grupo-formulario">
                <input
                  type="password"
                  class="campo-formulario"
                  id="password"
                  placeholder="Senha"
                  v-model="senha"
                  required
                />
              </div>
              <div class="grupo-formulario">
                <button type="submit" class="btn btn-primary btn-block">Entrar</button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
html, body {
  background-image: linear-gradient(to bottom, #347ec7, #162939); /* Dark gradient background */
  height: 100vh; /* Make sure to set height for html and body */
  margin: 0; /* Remove default margins */
}
.login-title {
    text-align: center; /* Center the title */
    font-size: 40px; /* Adjust font size as needed */
    margin-bottom: 20px; /* Add some margin below the title */
  }
/* Estilos da caixa de login */
.container {
  display: flex; /* Enable Flexbox layout */
  flex-direction: column; /* Arrange items vertically */
  align-items: center; /* Center items horizontally */
  justify-content: center; /* Center items vertically */
  height: 100vh; /* Make container full viewport height */
  margin: 0; /* Remove default margins */
}
.caixa-login {
  margin-top: 10px;
  background-color: #b2d0e9;
  padding: 100px;
  border-radius: 10px; /* Aumentar os cantos arredondados */
  box-shadow: 0 2px 5px rgba(179, 160, 160, 0.1);
  width: 400px; /* Adjust width as needed */
  max-width: 100%; /* Ensure it doesn't exceed 100% width */
  margin: 0 auto; /* Centralizar a caixa de login */
}

.corpo-caixa-login {
  /* Remover o plano de fundo branco padrão */
  background-color: transparent;
}

.grupo-formulario {
  margin-bottom: 20px;
}

/* Estilos dos campos de entrada */
.campo-formulario {
  border: 1px solid #ced4da;
  border-radius: 4px;
  padding: 10px;
  width: 100%;
}

.campo-formulario:focus {
  border-color: #3498db; /* Alterar a cor da borda ao focar */
  box-shadow: 0 0 0 2px rgba(52, 152, 219, 0.5); /* Adicionar um contorno sutil ao focar */
}

/* Estilos do botão de envio */
.btn.btn-primary {
  background-color: #3498db;
  border-color: #2980b9;
  transition: background-color 0.3s ease; /* Adicionar transição de hover */
  color: #fff;
  padding: 10px 20px;
  border-radius: 4px;
  width: 100%;
}

.btn.btn-primary:hover {
  background-color: #2980b9; /* Cor mais escura ao passar o mouse */
}
</style>

<script setup>
import { ref } from 'vue';

const nomeUsuario = ref('');
const senha = ref('');

const handleSubmit = () => {
  // Substitua esta lógica de placeholder pela sua lógica de login real
  // (por exemplo, enviar dados a uma API de back-end para autenticação)
  console.log('Formulário enviado:', { nomeUsuario: nomeUsuario.value, senha: senha.value });
};
</script>
