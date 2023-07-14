<template>
  <body>

    <header>
      <h3 class="logo">Residencia Universitaria Uleam</h3>
      <nav class="navigation">
        <RouterLink to="/inicio">Inicio</RouterLink>
        <RouterLink to="/uleam">Uleam</RouterLink>
        <RouterLink to="/habitaciones">Habitaciones</RouterLink>
        <RouterLink to="/perfil">Perfil</RouterLink>
        <button class="bntLogin-popup" @click="router.push('/')">Cerrar Sesión</button>
      </nav>
    </header>

    <main>
      <section class="inform">
        <img src="../assets/fondo.png" alt="fond">
        <h2>Somos su segundo hogar</h2>
        <h2>Bienvenidos a la Residencia Universitaria Uleam</h2>

        <p>Les damos la bienvenida a la residencia universitaria de la Uleam.</p>
        <p>Una residencia universitaria es un lugar donde los estudiantes pueden vivir mientras estudian en la
          universidad.</p>
        <p>Las residencias universitarias suelen estar ubicadas en el campus o cerca
          de él, lo que las hace convenientes para los estudiantes.</p>
        <p>Las residencias universitarias pueden ofrecer habitaciones individuales, dobles o compartidas.</p>
        <p>Además de las habitaciones, las residencias universitarias pueden ofrecer servicios
          como comedor, lavandería, acceso a Internet y actividades extracurriculares. Vivir en una
        residencia universitaria puede ser una oportunidad para conocer a otros estudiantes y hacer amigos.</p>
        <p>Tambien puede ser una forma mas económica de vivir mientras se estudia. Las residencias
          universitarias pueden ser una buena opción para los estudiantes de otras ciudades
        o país que necesitan un lugar para vivir mientras estudian en otra ciudad</p>
      </section>
    </main>
    <hr>
  </body>
</template>

<script setup>
import router from "../router";
import {RouterLink} from "vue-router";
</script>

<style scoped>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header {
  position: relative;
  background-color: #ff0000a0;
  top: 0;
  left: 0;
  padding: 10px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: rgba(255, 0, 0, 0.848);
  z-index: 99;
}

.logo {
  font-size: 2em;
  color: white;
  user-select: none;
  margin: 0;
}

.navigation {
  display: flex;
  justify-content: space-between;
  margin-top: 10px;
  /*ojo*/
  text-align: right;
}

.navigation a {
  position: relative;
  font-size: 1.1em;
  text-decoration: none;
  font-weight: 500;
  color: white;
  margin-left: 40px;
  /*fnaja roja tamaño*/
}

.navigation a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -6px;
  width: 100%;
  height: 3px;
  background: #ffffff;
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
  border: 2px solid #ffffff;
  outline: none;
  border-radius: 6px;
  font-size: 1.1em;
  color: #fff;
  cursor: pointer;
  font-weight: 500;
  margin-left: 40px;
  transition: .5s;
}

.main {
  padding: 20px;
}

.inform {
  text-align: center;
}

.inform h2 {
  color: black;
}

.inform p {
  margin-bottom: 10px;
}

.inform img {
  max-width: 100%;
  height: auto;
  margin-bottom: 20px;
}

footer {
  background-color: #333;
  color: #fff;
  padding: 10px;
  text-align: center;
}</style>