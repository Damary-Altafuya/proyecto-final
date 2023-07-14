<template>
  <body>
    <header>
      <h3 class="logo">Residencia Universitaria Uleam</h3>
      <nav class="navigation">
        <a href="../inicio.html">Inicio</a>
        <a href="proyecto/uleam.html">Uleam</a>
        <a href="#">Habitaciones</a>
        <a href="proyecto/perfil.html">Perfil</a>
        <button class="bntLogin-popup" onclick="cerrarSesion()">Cerrar Sesión</button>

      </nav>
    </header>
    <div class="container">
      <h2>Muestras de Habitaciones Individuales</h2>

      <section class="room">
        <img src="../assets/indiv.jpeg" alt="Habitación Individual 1">
        <h2>Habitación Individual</h2>
        <p>Una habitación individual para un estudiante universitario
          debe ser un espacio confortable, seguro y equipado con lo necesario</p>
        <p> para el estudio. Algunas características que pueden
          tener las habitaciones individuales para estudiantes universitarios son:</p>
        <p>- Cama individual</p>
        <p>- Escritorio y silla para estudiar</p>
        <p>- Conexión Wi-Fi</p>
        <p>- Televisión</p>
        <p>- Telefono directo en la habitacion</p>
        <p>- Nevera/minibar</p>
        <p>- Armario o espacio de almacenamiento</p>
        <p>- Baño privado con ducha o bañera y aseo</p>
        <p>Precio: $160 por mes.</p>
        <button @click="router.push('/reserva')" class="btn">Reservar</button>
      </section>

      <section class="room">
        <img src="../assets/doble.jpeg" alt="Habitación Individual 2">
        <h2>Habitación Doble</h2>
        <p>Una habitación doble para un estudiante universitario
          es una habitación que puede ser compartida con otra persona.
          Algunas características que pueden tener las habitaciones
          dobles para estudiantes universitarios son:</p>
        <p>- Dos camas individuales</p>
        <p>- Escritorio y silla para estudiar</p>
        <p>- Conexión Wi-Fi</p>
        <p>- Televisión</p>
        <p>- Telefono directo en la habitacion</p>
        <p>- Nevera/minibar</p>
        <p>- Armario o espacio de almacenamiento individuales</p>
        <p>- Baño privado con ducha o bañera y aseo</p>
        <p>Precio: $180 por mes.</p>
        <button @click="router.push('/reserva')" class="btn">Reservar</button>
      </section>

      <section class="room">
        <img src="../assets/compartida.jpg" alt="Habitación Individual 3">
        <h2>Habitación Compartida</h2>
        <p>Una habitación compartida para un estudiante universitario es una
          habitación que se comparte con varios estudiantes. Algunas características
          que pueden tener las habitaciones compartidas para estudiantes universitarios son:</p>
        <p>- Camas individual o literas</p>
        <p>- Escritorio y silla para estudiar</p>
        <p>- Conexión Wi-Fi</p>
        <p>- Televisión</p>
        <p>- Telefono directo en la habitacion</p>
        <p>- Nevera/minibar</p>
        <p>- Armario o espacio de almacenamiento individuales</p>
        <p>- Baño privado con ducha o bañera y aseo</p>
        <p>Precio: $210 por mes.</p>
        <button @click="router.push('/reserva')" class="btn">Reservar</button>
      </section>
    </div>
  </body>
</template>

<script setup>
import router from "../router";
import { RouterLink } from "vue-router";
</script>

<style scoped>
body {
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-size: cover;
  background-position: center;
}

.logo {
  font-size: 1.5em;
  color: white;
  user-select: none;
  margin-top: 20px;
  display: flex;
}

header {
  background: rgba(255, 0, 0, 0.848);
  padding: 20px;
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 99;
}

.container {
  margin-left: 30px;
  margin-bottom: 10px;
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

.h1,
h2 p {
  color: #000000;
  margin-top: 20px;
}

.container .room {
  margin-top: 25px;
  margin-left: 05px;
}

.room .btn {
  padding: 10px 15px;
  background-color: #44b347;
  color: white;
  border: none;
  outline: none;
  cursor: pointer;
  border-radius: 6px;

}

.room img {
  width: 300px;
  height: 300px;
  object-fit: cover;
  border-radius: 05px;
}

footer {
  background-color: #4f4c4c;
  color: #fff;
  padding: 10px;
  text-align: center;
}</style>