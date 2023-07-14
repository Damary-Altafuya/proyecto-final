<template>
  <body>
    <h1>Información del Estudiante</h1>

    <form @submit.prevent="reservar()">
      <label for="nombre">Nombre:</label>
      <input type="text" id="nombre" name="nombre" required><br><br>

      <label for="apellido">Apellido:</label>
      <input type="text" id="apellido" name="apellido" required><br><br>

      <label for="teléfono">Teléfono:</label>
      <input type="text" id="teléfono" name="teléfono" required><br><br>

      <label for="email">Correo:</label>
      <input type="email" id="email" name="email" required><br><br>

      <label for="habitacion">Tipo de Habitación:</label>
      <select id="habitacion" name="habitacion">
        <option value="individual">Individual</option>
        <option value="doble">Doble</option>
        <option value="compartida">Compartida</option>
      </select><br><br>

      <label for="fecha_inicio">Fecha de inicio:</label>
      <input type="date" id="fecha_inicio" name="fecha_inicio" required><br><br>

      <label for="fecha_fin">Fecha de fin:</label>
      <input type="date" id="fecha_fin" name="fecha_fin" required><br><br>

      <input type="submit" value="Reservar">
    </form>

    <footer>
      <p>Derechos de autor &copy; 2023 Residencia Universitaria Uleam</p>
    </footer>
  </body>
</template>

<script setup>
import router from "../router";
import { RouterLink } from "vue-router";

const reservar= ()=>{
  router.push('/inicio');
}
</script>

<style scoped>
body {
  font-family: 'Poppins', sans-serif;
  background-color: #f2f2f2;
  margin: 0;
  padding: 20px;
}

h1 {
  color: black;
  text-align: center;
}

form {
  max-width: 400px;
  margin: 0 auto;
  background-color: #fff;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
  margin-bottom: 10px;
}

input[type="text"],
input[type="email"],
select {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 3px;
  box-sizing: border-box;
  margin-bottom: 15px;
}

input[type="submit"] {
  background-color: #4CAF50;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 3px;
  cursor: pointer;
}

footer {
  text-align: center;
  margin-top: 20px;
  padding: 10px;
  background-color: #f2f2f2;
  color: #666;
  font-size: 14px;
}
</style>