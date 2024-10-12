<template>
    <v-container class="pa-4">
      <v-card class="mx-auto" max-width="1200" hover>
        <v-card-text>
          <v-row>
            <!-- Columna del título y subtítulo -->
            <v-col cols="12" md="4">
              <v-card-title class="text-h5">¿Qué hacemos?</v-card-title>
              <v-card-text class="description-text">En IEEE SPS UNI nos dedicamos a formar profesionales en el campo del procesamiento de señales,
                promoviendo la innovación tecnológica a través de actividades como charlas, talleres, proyectos 
                colaborativos y oportunidades de networking.
              </v-card-text>
            </v-col>
  
            <!-- Columna para los íconos y descripciones -->
            <v-col cols="12" md="8">
              <v-row class="d-flex justify-space-around">
                <v-col cols="12" sm="6" md="3" class="text-center">
                  <v-icon large color="purple">mdi-forum</v-icon>
                  <h3>Charlas</h3>
                  <p class="align-left">
                    Aprende de expertos en diversas áreas y participa en discusiones sobre los últimos avances tecnológicos.
                  </p>
                </v-col>
  
                <v-col cols="12" sm="6" md="3" class="text-center">
                  <v-icon large color="green">mdi-laptop</v-icon>
                  <h3>Talleres</h3>
                  <p class="align-left">
                    Participa en talleres prácticos donde desarrollarás habilidades técnicas aplicadas al procesamiento de señales.
                  </p>
                </v-col>
  
                <v-col cols="12" sm="6" md="3" class="text-center">
                  <v-icon large color="orange">mdi-account-network</v-icon>
                  <h3>Redes de contacto</h3>
                  <p class="align-left">
                    Conéctate con profesionales y estudiantes de todo el mundo.
                  </p>
                </v-col>
  
                <v-col cols="12" sm="6" md="3" class="text-center">
                  <v-icon large color="blue">mdi-account-group</v-icon>
                  <h3>Proyectos colaborativos</h3>
                  <p class="align-left">
                    Únete a equipos multidisciplinarios para desarrollar proyectos que resuelvan problemas reales.
                  </p>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-card-text>
      </v-card>
    </v-container>
  </template>
  
  <script>
  export default {
    name: "Beneficios",
  };
  </script>
  
  <style scoped>
  .mx-auto {
    margin: auto;
  }
  
  .v-card {
    padding: 16px;
  }
  
  .v-card-title {
    white-space: normal !important;
  }
  
  .description-text {
    white-space: normal;
    word-wrap: break-word;
    line-height: 1.6;
    text-align: justify; /* Justifica el texto */
  }
  .v-icon {
    margin-bottom: 11px;
  }
  </style>