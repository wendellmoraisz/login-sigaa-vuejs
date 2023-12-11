<template>
  <div id="app" class="container-fluid">
      <div class="col-md-6">
        <header>
          <img src="../assets/img/sigaa_img.jpeg" alt="Logo sigaa" width="200" height="200">
          <img src="../assets/img/ifpa_img.png" alt="Logo IFPA" width="200" height="200">
        </header>

        <h3 class="texto-title">Sistema Integrado de Gestão de Atividades Acadêmicas</h3>

        <div class="button-container">
          <a href="https://sig-treinamento.ifpa.edu.br/sigaa/verTelaLogin.do"><button class="btn btn-primary">SIGAA</button></a>
          <a href="https://sig-treinamento.ifpa.edu.br/sigaa/verTelaLogin.do"><button class="btn btn-primary">SIPAC</button></a>
          <a href="https://sig-treinamento.ifpa.edu.br/sigaa/verTelaLogin.do"><button class="btn btn-primary">SIGRH</button></a>
          <a href="https://sig-treinamento.ifpa.edu.br/sigaa/verTelaLogin.do"><button class="btn btn-primary">SIGPP</button></a>
          <a href="https://sig-treinamento.ifpa.edu.br/sigaa/verTelaLogin.do"><button class="btn btn-primary">SIGED</button></a>
          <a href="https://sig-treinamento.ifpa.edu.br/sigaa/verTelaLogin.do"><button class="btn btn-primary">SIGAdmin</button></a>
        </div>

        <div class="imagem-cadastro">
          <img src="../assets/img/professor.png" alt="Logo Professor" width="50" height="50">
          <img src="../assets/img/aluno.png" alt="Logo Aluno" width="50" height="50">
        </div>

        <div class="link-cadastro">
          <p>Professor ou Funcionário,<br>
            caso ainda não possua cadastro no SIGAA,<br>
            clique aqui</p>

          <p>Aluno, ou Egresso,<br>
            caso ainda não possua<br>
            cadastro no SIGAA,<br>
            clique aqui</p>
        </div>

        </div>

      <div class="col-md-6">
        <div class="login-container">
          <h1 class="login-title">BEM-VINDO</h1>
          <form @submit.prevent="login">
            <div class="mb-3">
              <label for="username" class="form-label">Usuário</label>
              <input type="text" v-model="username" class="form-control" id="username" required>
            </div>
            <div class="mb-3">
              <label for="password" class="form-label">Senha</label>
              <input type="password" v-model="password" class="form-control" id="password" required>
            </div>
            <button type="submit" class="btn btn-success">Entrar</button>

          </form>
          <div class="login-container">
            <a href="https://www.gov.br/pt-br"><button type="submit" class="btn btn-login-gov">Entrar com o GOV.BR</button></a>
          </div>
          <div class="button-container">
            <h3 class="recuperacao-title">OPÇÕES DE RECUPERAÇÃO</h3>
            <button class="btn btn-primary">Perdi meu e-mail de confirmação de cadastro</button>
            <button class="btn btn-primary">Esqueci meu login</button>
            <button class="btn btn-primary">Esqueci minha senha</button>
          </div>
          <p>Este sistema é melhor visualizado utilizando o Mozilla <br>
             Firefox, para baixá-lo e instalá-lo, <a href="https://www.mozilla.org/pt-BR/firefox/new/">clique aqui.</a></p>
          <p>Para visualizar documentos é necessário utilizar o<br>
             Adobe Reader, para baixá-lo e instalá-lo, <a href="https://www.adobe.com/br/acrobat/pdf-reader.html">clique aqui.</a></p>
        </div>
      </div>
  </div>
  <footer>
    <p>SIGAA | Diretoria de Tecnologia da Informação e Comunicação - | Copyright © 2006-2023 - IFPA - sigaa-d02 - v3.12</p>
  </footer>

</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {
    login() {
      console.log('Usuário:', this.username);
      console.log('Senha:', this.password);
    }
  }
};
</script>

<style scoped>

template {
  margin: 0;
  padding: 0;
}

#app {
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin: 0;
  box-sizing: border-box;
}

.container-fluid {
  padding: 0;
}

.col-md-6 {
  height: 100%;
  width: 100%;
}

/* Lado esquerdo com logos e botões */
.col-md-6:first-child {
  background-color: #fff;
  color: black;
  padding: 20px;
}

.button-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.btn-primary {
  background-color: #385378;
  color: #fff;
  border-radius: 10px;
}

.btn-primary:hover {
  background-color: #dcb078;
  color: #1e3a8a;
}

.texto-title {
  text-align: center;
}

.imagem-cadastro{
  display: flex;
  flex-direction: row;
  text-align: center;
  margin: 20px;

}
.link-cadastro {
  text-align: center;
  margin: 20px;
  display: flex;

}

/* Lado direito com formulário de login */
.col-md-6:last-child {
  background-color: #309c44;
  padding: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.mb-3 input {
  width: 100%;
  border-radius: 4px;
  padding: 12px;
  border: none;
}

.mb-3 input:focus {
  outline: none;
}

.mb-3 label {
  font-size: 16px;
  display: block;
}

.login-container {
  color: #fff;
  padding: 20px;
  text-align: center;
}

.login-container form {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.form-label {
  text-align: left;
  margin-bottom: 5px;
  width: 300px;
}

.form-control {
  margin-bottom: 10px;
}

.login-title {
  font-size: 2rem;
  margin-bottom: 20px;
}

.btn {
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
  font-style: bold;
  padding: 8px;
  border: none;
  width: 100%;
}

.btn-login-gov {
  background-color: #2245a7;
  color: #fff;
}

.btn-success {
  background-color: #e53935;
  color: #fff;
}

.recuperacao-title {
  font-size: 2rem;
  margin-bottom: 20px;
}

</style>
