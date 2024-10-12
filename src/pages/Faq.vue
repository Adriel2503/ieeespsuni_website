<template> 
    <v-container class="pa-5">
      <!-- Agrupar el título y el subtítulo en un div para organizar mejor -->
      <div class="faq-header">
        <!-- Título de la sección -->
        <h1 class="text-center custom-title">Preguntas Frecuentes</h1>
        <p class="subheading text-center custom-subtitle">
          ¿Necesita respuestas? Todo lo que necesitas saber se encuentra aquí.
        </p>
      </div>
  
      <!-- Contenedor adicional para la sección de FAQ con un ancho controlado -->
      <v-container class="faq-content" max-width="800px">
        <!-- Sección de FAQ con expansión utilizando el formato compacto -->
        <v-expansion-panels>
          <!-- Pregunta 1 -->
          <v-expansion-panel
            title="1. ¿Qué es IEEE SPS UNI?"
            text="IEEE SPS UNI es el capítulo estudiantil de la Sociedad de Procesamiento de Señales en la Universidad Nacional de Ingeniería. Nos enfocamos en promover el conocimiento y la aplicación de técnicas avanzadas en el procesamiento de señales."
          ></v-expansion-panel>
  
          <!-- Pregunta 2 -->
          <v-expansion-panel
            title="2. ¿Cómo puedo formar parte de IEEE SPS UNI?"
            text="Cualquier estudiante de la UNI puede unirse. Solo necesitas inscribirte a través de nuestro formulario en línea y estar dispuesto a participar activamente en proyectos y eventos."
          ></v-expansion-panel>
  
          <!-- Pregunta 3 -->
          <v-expansion-panel
            title="3. ¿Qué actividades organiza IEEE SPS UNI?"
            text="Organizamos charlas, talleres, proyectos colaborativos y Study Jams, entre otros eventos académicos que fomentan el aprendizaje y la colaboración entre los miembros."
          ></v-expansion-panel>
  
          <!-- Pregunta 4 -->
          <v-expansion-panel
            title="4. ¿Hay requisitos para participar en los eventos?"
            text="La mayoría de los eventos son abiertos a todos los estudiantes. Sin embargo, algunos talleres especializados pueden requerir conocimientos técnicos previos para aprovechar al máximo las actividades."
          ></v-expansion-panel>
  
          <!-- Pregunta 5 -->
          <v-expansion-panel
            title="5. ¿Puedo participar si soy de otra universidad?"
            text="Nuestros eventos están dirigidos principalmente a estudiantes de la UNI, pero algunos eventos pueden estar abiertos a estudiantes de otras universidades. Te recomendamos revisar la descripción de cada evento para confirmar."
          ></v-expansion-panel>
  
          <!-- Pregunta 6 -->
          <v-expansion-panel
            title="6. ¿Cuánto cuestan los eventos y talleres?"
            text="La mayoría de los eventos son gratuitos para los miembros de IEEE SPS UNI. Sin embargo, algunos talleres especializados pueden tener un costo asociado para cubrir materiales y otros gastos."
          ></v-expansion-panel>
  
          <!-- Pregunta 7 -->
          <v-expansion-panel
            title="7. ¿Hay certificados por participar en los eventos?"
            text="Sí, algunos talleres y eventos ofrecen certificados de participación, especialmente aquellos que implican la realización de proyectos o la adquisición de nuevas habilidades técnicas."
          ></v-expansion-panel>
  
          <!-- Pregunta 8 -->
          <v-expansion-panel
            title="8. ¿Qué beneficios obtengo al unirme a IEEE SPS UNI?"
            text="Al unirte, obtienes acceso a una red de contactos profesionales, oportunidades de aprendizaje continuo, participación en proyectos innovadores y la posibilidad de desarrollar habilidades técnicas y de liderazgo."
          ></v-expansion-panel>
  
          <!-- Pregunta 9 -->
          <v-expansion-panel
            title="9. ¿Cómo puedo proponer un proyecto dentro del capítulo?"
            text="Si tienes una idea de proyecto, puedes compartirla con el equipo directivo a través de nuestro formulario de propuestas o asistir a nuestras reuniones semanales para discutirla y evaluar su implementación."
          ></v-expansion-panel>
  
          <!-- Pregunta 10 -->
          <v-expansion-panel
            title="10. ¿Qué temas cubren los talleres y eventos de IEEE SPS UNI?"
            text="Cubrimos una amplia variedad de temas como procesamiento de imágenes, inteligencia artificial, machine learning, señales acústicas, análisis de datos y otras áreas avanzadas del procesamiento de señales."
          ></v-expansion-panel>
        </v-expansion-panels>
      </v-container>
    </v-container>
  </template>
  
  <script>
  export default {
    name: "Faq",
  };
  </script>
  
  <style scoped>
  .text-center {
    text-align: center;
  }
  
  /* Clase personalizada con mayor especificidad */
  h1.custom-title {
    font-size: 3rem; /* Ajusta este valor según tus necesidades */
    font-weight: bold; /* Opcional */
  }
  
  /* Estilos adicionales para el subtítulo (párrafo) */
  p.custom-subtitle {
    font-size: 1.5rem; /* Tamaño del texto personalizado */
    font-weight: normal; /* Puedes cambiarlo a 'bold' si prefieres negrita */
    color: #555; /* Color de texto, ajusta según lo necesites */
    margin-top: 10px; /* Ajuste del espacio superior */
    margin-bottom: 60px; /* Aumentar el espacio inferior entre subtítulo y preguntas */
  }
  
  /* Estilos adicionales para el contenedor del título y subtítulo */
  .faq-header {
    margin-top: 10px; /* Añadir espacio arriba del título y subtítulo */
    margin-bottom: 40px; /* Ajusta el espacio debajo del encabezado */
  }
  
  /* Estilos adicionales para el contenedor de FAQ */
  .faq-content {
    margin-top: 20px; /* Añade espacio superior entre el título/subtítulo y el contenido */
    max-width: 800px; /* Limitar el ancho máximo del contenedor de preguntas */
    margin-left: auto;
    margin-right: auto; /* Centramos el contenido horizontalmente */
  }
  
  /* Añadir sombra suave y bordes redondeados al panel de FAQ */
  .v-expansion-panels {
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1); /* Sombra suave */
    border-radius: 8px; /* Bordes redondeados */
  }
  </style>
  