<template>
    <v-container>
      <v-row>
        <!-- Primera tarjeta (¿Quiénes somos?) -->
        <v-col cols="12" md="4" class="d-flex justify-center">
          <v-card class="pa-4 d-flex flex-column align-center" rounded="lg" hover>
            <v-card-title class="text-h5 text-center primary--text">¿Quiénes somos?</v-card-title>
            <v-card-text class="justify-text">
              IEEE SPS UNI es un capítulo estudiantil dedicado al avance del procesamiento de señales. Desarrollamos proyectos en áreas como IA, procesamiento de imágenes, audio y acústica, seguridad de la información, procesamiento de lenguaje natural y Machine Learning, contribuyendo a la innovación en una amplia gama de aplicaciones tecnológicas.
            </v-card-text>
          </v-card>
        </v-col>
  
        <!-- Segunda tarjeta (Misión) -->
        <v-col cols="12" md="4" class="d-flex justify-center">
          <v-card class="pa-4 d-flex flex-column align-center" rounded="lg" hover>
            <v-card-title class="text-h5 text-center primary--text">Misión</v-card-title>
            <v-card-text class="justify-text">
              Fomentar la formación de estudiantes en el procesamiento de señales a través de proyectos innovadores, investigación científica y actividades académicas. Buscamos crear un entorno colaborativo que permita aplicar conocimientos y generar soluciones tecnológicas con impacto en el ámbito académico y profesional, impulsando el avance tecnológico.
            </v-card-text>
          </v-card>
        </v-col>
  
        <!-- Tercera tarjeta (Visión) -->
        <v-col cols="12" md="4" class="d-flex justify-center">
          <v-card class="pa-4 d-flex flex-column align-center" rounded="lg" hover>
            <v-card-title class="text-h5 text-center primary--text">Visión</v-card-title>
            <v-card-text class="justify-text">
              Ser líderes en la formación de profesionales capaces de enfrentar desafíos tecnológicos, destacándonos por la innovación en el procesamiento de señales. Aspiramos a contribuir con soluciones avanzadas que impacten positivamente en la sociedad, fomentando el aprendizaje continuo y colaboraciones con la industria y el sector académico.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: "Pre",
  };
  </script>
  
  <style scoped>
  .justify-text {
    text-align: justify;
  }
  </style>
  