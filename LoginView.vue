<template>
  <body>

    <header>
      <h2 class="logo"><img src="../assets/uleam.png" alt=""></h2>
      <nav class="navigation">
        <RouterLink to="/inicio">Inicio</RouterLink>
        <RouterLink to="/uleam">Uleam</RouterLink>
        <RouterLink to="/habitaciones">Habitaciones</RouterLink>
        <button class="bntLogin-popup" @click="router.push('/registro')">Registrarse</button>
      </nav>
    </header>

    <div class="wrapper">
      <div class="form-box login">
        <h2>Iniciar Sesión</h2>
        <form @submit.prevent="enviarFormulario()">

          <div class="input-box">
            <span class="icon"><ion-icon name="person"></ion-icon></span>
            <input type="email" id="usuario" required>
            <label>Usuario</label>
          </div>

          <div class="input-box">
            <span class="icon"><ion-icon name="lock-closed"></ion-icon></span>
            <input type="password" id="contraseña" required>
            <label>Contraseña</label>
          </div>

          <div class="remember-forgot">
            <label><input type="checkbox">Recuérdame</label>
            <a href="#">¿Olvidaste tu contraseña?</a>
          </div>

          <button @click="" type="submit" class="btn">Acceder</button>
          <div class="login-register">
            <p>¿No tienes cuenta?<RouterLink to="/registro" class="register-link">Registrar</RouterLink>
            </p>
          </div>

        </form>
      </div>
    </div>    
    
  </body>
</template>

<script setup>
import router from "../router";
import {RouterLink} from "vue-router";

const enviarFormulario = ()=>{
  router.push('/inicio')
}
</script>

<style scoped>
body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: url(../assets/uleam.jpeg) no-repeat;
    background-size: cover;
    background-position: center;
}
header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px 100px;
    background: rgba(255, 0, 0, 0.848);
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 99;
}
.logo{
    font-size: 2em;
    color: white;
    user-select: none;
    flex-wrap: wrap;
    user-select: none;
}
.navigation a {
    position: relative;
    font-size: 1.1em;
    color: white;
    text-decoration: none;
    font-weight: 500;
    margin-left: 40px;
}
.navigation a::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: -6px;
    width: 100%;
    height: 3px;
    background: #fff;
    border-radius: 5px;
    transform-origin: right;
    transform: scaleX(0);
    transition: transform .5s;
}
.navigation a:hover::after {
    transform-origin: left;
    transform: scaleX(1);
}
.navigation .bntLogin-popup {
    width: 130px;
    height: 50px;
    background: transparent;
    border: 2px solid #fff;
    outline: none;
    border-radius: 6px;
    cursor: pointer;
    font-size: 1.1em;
    color: #fff;
    font-weight: 500;
    margin-left: 40px;
    transition: .5s;
}
.navigation .bntLogin-popup:hover {
    background: #fff;
    color: #162938;
}

.wrapper {
    z-index: 999;
    position: relative;
    width: 400px;
    height: 440px;
    background: transparent;
    border: 2px solid rgba(225, 225, 225, .5);
    border-radius: 20px;
    backdrop-filter: blur(20px);
    box-shadow: 0 0 30px rgba(0, 0, 0, .5);
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    transition: height .2 ease;
}
.wrapper .form-box {
    width: 100%;
    padding: 40px;
}
.wrapper .icon-close {
    position: absolute;
    top: 0;
    right: 0;
    width: 45px;
    height: 45px;
    background: #ff000078;
    font-size: 2em;
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    border-bottom-left-radius: 20px;
    cursor: pointer;
    z-index: 1;
}
.form-box h2 {
    font-size: 2em;
    color: #162938;
    text-align: center;
}
.input-box {
    position: relative;
    width: 100%;
    height: 50px;
    border-bottom: 2px solid #000000;
    margin: 30px 0;
}
.input-box label {
    position: absolute;
    top: 50%;
    left: 5px;
    transform: translateY(-50%);
    font-size: 1em;
    color: #000000;
    font-weight: 500;
    pointer-events: none;
    transition: .5s;
}
.input-box input:focus~label,
.input-box input:valid~label {
    top: -5px;
}
.input-box input {
    width: 100%;
    height: 100%;
    background: transparent;
    border: none;
    outline: none;
    font-size: 1em;
    color: #162938;
    font-weight: 600;
    padding: 0 35px 0 5px;
}
.input-box .icon {
    position: absolute;
    right: 8px;
    font-size: 1.2em;
    color: #162938;
    line-height: 57px;
}
.remember-forgot {
    font-size: .9em;
    color: #000000;
    font-weight: 500;
    margin: -15px 0 15px;
    display: flex;
    justify-content: space-between;
}
.remember-forgot label input {
    accent-color: #000000;
    margin-right: 3px;
}
.remember-forgot a {
    color: #000000;
    text-decoration: none;
}
.btn {
    width: 100%;
    height: 45px;
    background: #f200008a;
    border: none;
    outline: none;
    border-radius: 6px;
    cursor: pointer;
    font-size: 1em;
    color: #ffffff;
    font-weight: 500;
}
.login-register {
    font-size: .9em;
    color: #000000;
    text-align: center;
    font-weight: 500;
    margin: 25px 0 10px;
}
.login-register p a {
    color: #000000;
    text-decoration: none;
    font-weight: 600;
}
.login-register p a:hover {
    text-decoration: underline;
}
</style>