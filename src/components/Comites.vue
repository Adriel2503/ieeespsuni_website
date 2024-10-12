<template>
    <v-container>
      <!-- Card principal con el título de la sección -->
      <v-row justify="center">
        <v-col cols="12">
          <v-card outlined hover class="pa-5 mx-auto">
            <v-row class="d-flex align-center">
              <v-col class="d-flex align-center">
                <v-card-title class="headline">
                  Comités Técnicos (TCs)
                </v-card-title>
                <v-icon
                  class="ml-2"
                  color="lime darken-2"
                  large
                  aria-label="Configuración de Comités Técnicos"
                >
                  mdi-cog-outline
                </v-icon>
              </v-col>
            </v-row>
            <v-card-text class="text-justify">
              La Sociedad de Procesamiento de Señales (SPS) cuenta con varios Comités Técnicos y Grupos de Trabajo Técnico (TWGs) que abarcan una amplia gama de actividades relacionadas con el procesamiento de señales en áreas específicas. Estos comités permiten que individuos con intereses técnicos similares se reúnan para compartir ideas, colaborar en investigaciones, y desarrollar una fuerte red de contactos profesionales. Los Comités Técnicos están involucrados en múltiples actividades que incluyen la organización de conferencias, publicaciones y premios, además de influir en decisiones claves dentro de la Sociedad.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
  
      <!-- Tarjetas dinámicas para cada Comité Técnico -->
      <v-row>
        <v-col
          v-for="committee in committees"
          :key="committee.id"
          cols="12"
          md="4"
        >
          <CommitteeCard :title="committee.title" :description="committee.description" />
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  import CommitteeCard from './CommitteeCard.vue';
  
  export default {
    components: {
      CommitteeCard
    },
    data() {
      return {
        committees: [
          {
            id: 1,
            title: "Applied Signal Processing Systems",
            description: "Promueve sistemas eficientes para el procesamiento de señales, como GPUs, ASICs, FPGAs, y tecnologías emergentes como computación neuromórfica y cuántica. También se enfoca en aplicaciones de sistemas y modelado avanzado de procesamiento de señales."
          },
          {
            id: 2,
            title: "Audio and Acoustic Signal Processing",
            description: "Se centra en el desarrollo científico y tecnológico del procesamiento de señales de audio y acústicas, abarcando desde el procesamiento de arrays de micrófonos hasta el aprendizaje automático y la psicoacústica. Sus aplicaciones incluyen dispositivos electrónicos de consumo y clasificación de géneros musicales."
          },
          {
            id: 3,
            title: "Bio Imaging and Signal Processing Technical Committee",
            description: "Impulsa avances en el procesamiento de imágenes y señales biomédicas, abarcando campos como la microscopía, bioinformática e imágenes médicas. Además, apoya el desarrollo de tratamientos guiados por imágenes y técnicas de análisis computacional."
          },
          {
            id: 4,
            title: "Computational Imaging",
            description: "Se enfoca en la creación de imágenes mediante técnicas computacionales avanzadas, diferenciándose del procesamiento de imágenes tradicional al integrar el cálculo en el proceso de formación de imágenes."
          },
          {
            id: 5,
            title: "Image, Video, and Multidimensional Signal Processing",
            description: "Promueve el procesamiento avanzado de imágenes, video y señales multidimensionales, liderando programas técnicos en ICIP e ICASSP. Organiza talleres, evalúa nominaciones para premios y conferencistas, y contribuye al desarrollo de estándares IEEE."
          },
          {
            id: 6,
            title: "Information Forensics and Security",
            description: "Este comité se enfoca en el análisis forense de la información y en la seguridad, desarrollando técnicas avanzadas para proteger y verificar la integridad de datos en diversas aplicaciones."
          },
          {
            id: 7,
            title: "Machine Learning for Signal Processing",
            description: "Se especializa en desarrollar metodologías de aprendizaje automático aplicadas al procesamiento de señales, abarcando áreas como análisis de señales no lineales y adaptativas. Sus aplicaciones incluyen audio, imágenes, señales biomédicas y genómicas, entre otras."
          },
          {
            id: 8,
            title: "Multimedia Signal Processing",
            description: "El comité se centra en el procesamiento de señales multimedia, abarcando audio, video e imágenes. Promueve el avance tecnológico organizando talleres y conferencias como el IEEE MMSP, y colabora con otras sociedades en publicaciones y eventos multimedia."
          },
          {
            id: 9,
            title: "Sensor Array and Multichannel",
            description: "Promueve el procesamiento de arrays de sensores y señales multicanal, incluyendo técnicas como beamforming, estimación de dirección de llegada, sistemas MIMO y aplicaciones en radar, sonar y sistemas biomédicos. También abarca la separación ciega de fuentes y sistemas multisensoriales inteligentes."
          },
          {
            id: 10,
            title: "Signal Processing for Communications and Networking",
            description: "Se enfoca en las intersecciones entre procesamiento de señales y comunicaciones, abarcando áreas como codificación, compresión de datos, modelado de canales, comunicaciones inalámbricas y redes distribuidas. También aborda redes ad-hoc, radio cognitivo y optimización de recursos en sistemas de comunicación."
          },
          {
            id: 11,
            title: "Signal Processing Theory and Methods",
            description: "Impulsa el desarrollo teórico en procesamiento digital de señales y análisis estadístico, abarcando áreas como filtrado digital, procesamiento adaptativo, estimación y detección. También organiza talleres y sesiones especiales, además de revisar publicaciones en ICASSP."
          },
          {
            id: 12,
            title: "Speech and Language Processing",
            description: "Aborda el procesamiento del habla y el lenguaje, cubriendo áreas como reconocimiento de voz, síntesis de texto a voz, comprensión del lenguaje hablado y traducción de voz a voz. Organiza sesiones técnicas en ICASSP y talleres especializados como ASRU y SLT."
          },
        ]
      };
    },
  };
  </script>
  
  <style>
  </style>
  