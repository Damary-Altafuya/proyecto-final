<template>
  <body>

    <header>
      <h2 class="logo"><img src="../assets/uleam.png" alt=""></h2>
      <nav class="navigation">
        <RouterLink to="/inicio">Inicio</RouterLink>
        <RouterLink to="/uleam">Uleam</RouterLink>
        <RouterLink to="/habitaciones">Habitaciones</RouterLink>
        <button @click="router.push('/')" class="bntLogin-popup">Cerrar Sesión</button>
      </nav>
    </header>

    <div class="wrapper">
      <div class="form-box">
        <h2>Registrarse</h2>
        <form @submit.prevent="enviarFormulario()">

          <div class="input-box">
            <span class="icon"><ion-icon name="person"></ion-icon></span>
            <input type="text" required>
            <label>Usuario</label>
          </div>

          <div class="input-box">
            <input type="text" required>
            <label>Nombres</label>
          </div>

          <div class="input-box">
            <input type="text" required>
            <label>Apellidos</label>
          </div>

          <div class="input-box">
            <input type="date" required>
            <label>Fecha nacimiento</label>
          </div>

          <div class="input-box">
            <input type="email" required>
            <label>Correo</label>
          </div>

          <div class="input-box">
            <input type="password" required>
            <label>Contraseña</label>
          </div>

          <div class="remember-forgot">
            <label><input type="checkbox">Aceptar los Términos y Concidiciones</label>

          </div>

          <button type="submit" class="btn">Registrarse</button>
        </form>
      </div>
    </div>

  </body>
</template>

<script setup>
import router from "../router";
import {RouterLink} from "vue-router";

const enviarFormulario = ()=>{
  router.push('/')
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
header{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px;
    display: flex;
    background: rgba(255, 0, 0, 0.848);
    justify-content: space-between;
    align-items: center;
    z-index: 99;
}
.logo{
    user-select: none;
    display: flex;
    flex-wrap: wrap;
    margin-top: 20px;
}
.logo img {
    height: 70px;
    margin-right: 50px;
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
    background: white;
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
    border: 2px solid white;
    outline: none;
    border-radius: 6px;
    cursor: pointer;
    font-size: 1.1em;
    color: white;
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
    padding: 2rem 1rem;
    position: relative;
    width: 500px 0;
    height:  100vh;
    background: transparent;
    border: 2px solid rgba(225, 225, 225, .5);
    border-radius: 20px;
    backdrop-filter: blur(20px);
    box-shadow: 0 0 30px rgba(0, 0, 0, .5);
    display: flex;
    justify-content: center;
    align-items: center;
    transition: height .2 ease;
    height: 100vh;
}
.wrapper .form-box {
    width: 200%;
    padding: 80px;
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
    margin: 30px;
}
.input-box label {
    position: absolute;
    top: 50%;
    left: 5px;
    transform: translate(-50%);
    font-size: 0.9em;
    color: black;
    font-weight: 100;
    pointer-events: none;
    transition: .5s;
}
.input-box input:focus~label,
.input-box input:valid~label {
    top: -5px;
}
.input-box input {
    width: 50%;
    height: 50%;
    background: transparent;
    border: none;
    outline: none;
    font-size: 0.9em;
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
    margin-bottom: 10px;
}
.remember-forgot label input {
    accent-color: #000000;
    margin-right: 3px;
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
</style>