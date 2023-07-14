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
        <p>Es una residencia con años de experiencia en alojamiento a estudiantes
          ecuatorianos y extranjeros</p>
        <p>brindándoles seguridad en un ambiente
          familiar para satisfacción de residentes.</p>
      </section>
    </main>
    <main>
      <section class="presentacion">

        <h2>Acceso a la Residencia</h2>
        <RouterLink to="/reserva">Reservar habitación</RouterLink>
      </section>

      <section class="habitaciones">
        <ul>
          <li>
            <h2>Nuestras Habitaciones</h2>
            <br> <span>El servicio de Residencia Universitaria es
              únicamente para estudiantes de nuestra universidad.</span> 
            <span>Las habitaciones estarán adecuadas con cama,
              velador, cortinas y equipos. Los residentes deberán
              traer sus sábanas y toallas.</span>
            <span>Los residentes son responsables de los equipos,
              muebles y enseres de la Residencia y de las áreas sociales. En caso de pérdida</span> 
            y mal uso de los mismos, el valor correspondiente será asumido por el responsable, y en
            caso de no haberlo por los huéspedes de manera proporcional del costo.
            <span>El residente debe reportar inmediatamente a la administración
              cualquier anomalía o desperfecto en los enseres o en la habitación.</span>
            <span>El ingreso a las residencias es solo y exclusivamente para
              las personas que habitan en ella, y para visitantes con autorización, queda 
            terminantemente prohibido el ingreso de personas extrañas o
            estudiantes no autorizados.</span>

            <div class="img">
              <img src="../assets/one1.jpg" alt="Habitación">
              <img src="../assets/duo2.jpg" alt="Habitación">
              <img src="../assets/duo1.jpg" alt="Habitación">
              <img src="../assets/one.jpg" alt="Habitación">
              <img src="../assets/duo.jpg" alt="Habitación">
            </div>
          </li>

          <li>
            <h3>Forma de contratación</h3>
            <p>Depósito de 2 meses, que en caso de que existan daños serán cobrados;
              mínimo de contratación un semestre académico. Se exceptuará el tiempo de
            contratación, en el caso de programas especiales de estudiantes que
            vienen del extranjero. No se realizará reembolso alguno, por el pago en mención.
            En caso de tener el interés de pre-cancelar el año completo, se otorgará
            un descuento de 15%.</p>
          </li>
        </ul>
      </section>

      <section class="contactos">

        <h3>Contacto</h3>
        <p>Dirección: Av. Circunvalación Vía a San Mateo</p>
        <p>Manta - Manabí - Ecuador</p>
        <p>2623740 - 2620288</p><span class="icon"><ion-icon name="call"></ion-icon></span>
        <p>incidencias.diit@uleam.edu.ec</p>
      </section>
    </main>

    <footer>
      <p>Derechos de autor &copy; 2023 Residencia Universitaria Uleam</p>
    </footer>
  </body>
</template>

<script setup>
import router from "../router";
import {RouterLink} from "vue-router";
</script>

<style scoped>

body {
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-size: cover;
  background-position: center;
}
.logo{
  font-size: 2em;
  color: white;
  user-select: none;
  margin: 0;
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
  border: 2px solid #fff;
  outline: none;
  border-radius: 6px;
  cursor: pointer;
  font-size: 1.1em;
  color: #ffffff;
  font-weight: 500;
  margin-left: 40px;
  transition: .5s;
}
header {
  background-color: #ff0000a0;
  padding: 20px;
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 99;
  background: rgba(255, 0, 0, 0.848);
} 
.h1, h2 {
    color: #000000;
}
a {
    text-decoration: none;
    color: #000000;
}
.inform {
  background-color: white;/*fondo de foto*/
  padding: 60px;
  border: 2px solid #918585a7;
}
.inform img {
  max-width: 100%;
  height: auto;
  margin-bottom: 20px;
}
.inform h2 {
  text-align: center;
  color: #000000;
}
.inform p {
  text-align: center;
  margin-bottom: 10px;
}
.presentacion {
  background-color: #9f9f9f9b;
  padding: 50px;
}
.presentacion h2 {
  color: black;
  margin-bottom: 10px;
}
.presentacion a {
  background-color: #ff0000a0;
  color: white;
  border-radius: 6px;
  padding: 10px 20px;
  text-decoration: none;
}
.habitaciones {
  padding: 70px 30px;
  margin-top: 40px;
}
.habitaciones ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
.habitaciones h2 h3 {
  color: black;
}
.habitaciones span {
  display: block;
  margin-bottom: 10px;
}
.img {
  display: flex;
  flex-wrap: wrap;
  margin-top: 20px;
}
.img img {
  width: 200px;
  height: auto;
  margin-right: 10px;
  margin-bottom: 10px;
} 
.contactos {
  background-color: #e5e5e5ac;
  padding: 20px;
  border: 2px solid #918585;
}
.contactos h3 {
  color: #333;
}
.contactos p {
  margin-bottom: 10px;
}
footer {
  background-color: #4f4c4c;
  color: #fff;
  padding: 10px;
  text-align: center;
}
</style>