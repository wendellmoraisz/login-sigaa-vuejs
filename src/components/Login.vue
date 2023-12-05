<template>
  <div id="app" class="container-fluid">
      <div class="col-md-6">
        <header>
          <img src="logo1.png" alt="Logo 1">
          <img src="logo2.png" alt="Logo 2">
        </header>
        <div class="button-container">
          <button class="btn btn-primary">SIGAA</button>
          <button class="btn btn-primary">SIPAC</button>
          <button class="btn btn-primary">SIGRH</button>
          <button class="btn btn-primary">SIGPP</button>
          <button class="btn btn-primary">SIGED</button>
          <button class="btn btn-primary">SIGAdmin</button>
        </div>
      </div>

      <div class="col-md-6">
        <div class="login-container">
          <h2 class="login-title">Bem-Vindo</h2>
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
            <button type="submit" class="btn btn-login-gov">Entrar com o GOV.BR</button>
          </form>
        </div>
      </div>
  </div>
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
  padding: 20px;
}

.button-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.btn-primary {
  background-color: #1e3a8a;
  color: #fff;
  border-radius: 10px;
}

.btn-primary:hover {
  background-color: #dcb078;
  color: #1e3a8a;
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

</style>

