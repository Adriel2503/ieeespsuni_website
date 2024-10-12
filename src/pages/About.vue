<template>
  <v-container class="pa-5">
    <!-- Título principal -->
    <h1 class="text-center custom-title mb-5">About IEEE SPS UNI</h1>

    <!-- Sección de contenido en dos columnas -->
    <v-row>
      <!-- Columna 1: Texto descriptivo -->
      <v-col cols="12" md="6">
        <p class="body-1 mb-4 justify-text">
          IEEE SPS UNI es el capítulo estudiantil de la Sociedad de Procesamiento de Señales de la Universidad Nacional de Ingeniería. Nos dedicamos a promover el conocimiento y la aplicación de técnicas avanzadas en el procesamiento de señales.
        </p>
        <p class="body-1 mb-4 justify-text">
          Llevamos a cabo talleres, seminarios y proyectos de investigación que ayudan a los estudiantes a adquirir habilidades técnicas, trabajar en equipo, y mejorar sus capacidades para enfrentar retos del mundo real.
        </p>
        <p class="body-1">
          ¿Tienes preguntas o quieres unirte? Contáctanos en 
          <a href="mailto:ieeesps@uni.edu.pe" class="email-link">ieeesps@uni.edu.pe</a>.
        </p>
      </v-col>

      <!-- Columna 2: Imagen -->
      <v-col cols="12" md="6">
        <v-img
          src="@/assets/Ponentes.jpg"
          alt="Imagen de IEEE SPS UNI"
          class="rounded-img"
          max-height="350"
        ></v-img>
      </v-col>
    </v-row>

    <!-- Sección de botones de redes sociales -->
    <div class="social-section text-center mt-5">
      <h3 class="mb-3">Contáctenos</h3>
      <v-btn
        class="mx-2 social-btn"
        href="https://api.whatsapp.com/send?phone=51933511222"
        target="_blank"
        rel="noopener noreferrer"
        icon
      >
        <v-icon>mdi-whatsapp</v-icon>
      </v-btn>
      <v-btn
        class="mx-2 social-btn"
        href="https://www.linkedin.com/company/ieee-sps-uni/"
        target="_blank"
        rel="noopener noreferrer"
        icon
      >
        <v-icon>mdi-linkedin</v-icon>
      </v-btn>
      <v-btn
        class="mx-2 social-btn"
        href="https://www.facebook.com/IEEESPSUNI"
        target="_blank"
        rel="noopener noreferrer"
        icon
      >
        <v-icon>mdi-facebook</v-icon>
      </v-btn>
      <v-btn
        class="mx-2 social-btn"
        href="https://www.instagram.com/ieee_sps_uni/"
        target="_blank"
        rel="noopener noreferrer"
        icon
      >
        <v-icon>mdi-instagram</v-icon>
      </v-btn>
      <v-btn
        class="mx-2 social-btn"
        href="https://github.com"
        target="_blank"
        rel="noopener noreferrer"
        icon
      >
        <v-icon>mdi-github</v-icon>
      </v-btn>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "AboutIEEE",
};
</script>

<style scoped>
.custom-title {
  font-size: 3rem;
  font-weight: bold;
  margin-top: 10px;
}

.email-link {
  color: #1976D2;
  text-decoration: none;
}

.email-link:hover {
  text-decoration: underline;
}

.rounded-img {
  border-radius: 10px;
}

.justify-text {
  text-align: justify;
}

/* Siempre blanco el fondo de los botones y negro los íconos */
.social-section .social-btn {
  background-color: #ffffff; /* Fondo siempre blanco */
  border-radius: 50%;
  padding: 10px;
  color: #000000; /* Íconos siempre negros */
  transition: transform 0.3s ease, background-color 0.3s ease; /* Transición añadida */
}

/* Hover: cambia ligeramente el fondo y aumenta el tamaño */
.social-section .social-btn:hover {
  background-color: #e0e0e0; /* Fondo gris claro al hacer hover */
  transform: scale(1.1); /* Aumenta el tamaño del botón ligeramente */
}
</style>
