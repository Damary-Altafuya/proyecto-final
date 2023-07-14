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
    <div class="container">
      <h2>Perfil de Estudiante Universitario</h2>
      <h2>Información Personal</h2>

      <form action="procesar.php" method="POST">
        <div class="wrapper">

          <label for="nombre">Nombre:</label>
          <input type="text" id="nombre" name="nombre" value="" required><br><br>

          <label for="apellido">Apellido:</label>
          <input type="text" id="apellido" name="apellido" value="" required><br><br>

          <label for="fechanac">Fecha nacimiento:</label>
          <input type="date" id="fechanac" name="fechanac" value="" required><br><br>

          <label for="correo">Email:</label>
          <input type="email" id="correo" name="correo" value="" required><br><br>

          <label for="telefono">Teléfono:</label>
          <input type="text" id="telefono" name="telefono" value="" required><br><br>

          <h2>Información Académica</h2>
          <ul>
            <label for="facultad">Facultad:</label>
            <input type="text" id="facultad" name="facultad" value="" required><br><br>

            <label for="carrera">Carrera:</label>
            <input type="text" id="carrera" name="carrera" value="" required><br><br>

            <label for="periodo">Periodo:</label>
            <input type="text" id="periodo" name="periodo" value="" required><br><br>
          </ul>

          <h2>Dirección Residencia</h2>
          <ul>
            <label for="direccion">Dirección</label>
            <input type="text" id="direccion" name="direccion" value="" required><br><br>

            <input type="submit" value="Guardar Cambios">
          </ul>
        </div>
      </form>
    </div>
  </body>
</template>

<script setup>
import router from "../router";
import {RouterLink} from "vue-router";
</script>

<style scoped>
body{
	align-items: center;
	min-height: 100vh;
	justify-content: center;
	background-size: cover;
    background-position: center;
}
.logo {
	font-size: 2em;
	color: white;
	user-select: none;
}
header {
	padding: 20px;
	position: relative;
	top: 0;
	left: 0;
	width: 100%;
	display: flex;
	justify-content: space-between;
	align-items: center;
	background: rgba(255, 0, 0, 0.848);
	z-index: 99;
}
.container{
	margin-left: 30px;
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

.h2 {
	margin-top: 20px;
}
  
.wrapper input {
	display: block;
	margin-bottom: 5px;
	border-radius: 10px;
	position: relative;
	border: 2px solid rgba(201, 201, 201, 0.9);
}
  
input[type="submit"] { /*boton guardar */
	padding: 10px 20px;
	background-color: #f200009d;
	color: white;
	border: none;
	cursor: pointer;
	border-radius: 6px;
	font-weight: 500;
}
  
.logo {
	user-select: none;
    display: flex;
    flex-wrap: wrap;
    margin-top: 20px;
} 
form {
	margin-top: 50px;
	max-width: 500px;
}
  input[type="text"],
  input[type="email"],
  input[type="date"] {
	width: 100%;
	padding: 10px;
	margin-bottom: 10px;
	box-sizing: border-box;
} 
ul {
	list-style: none;
	padding: 0;	
}
ul label {
	display: inline-block;
	width: 120px;
}
</style>