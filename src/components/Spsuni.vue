<template>
  <v-container class="pa-3">
    <div class="hero-header">
      <h1 class="text-center custom-title">
        <span class="green">IEEE</span> <span class="blue">SPS UNI</span>
      </h1>
      <p class=" text-center subheading custom-subtitle">
        Capítulo estudiantil de la Sociedad de Procesamiento de Señales de la Universidad Nacional de Ingeniería
      </p>
    </div>
  </v-container>
</template>

<script setup>
  //
</script>

<style scoped>
.text-center {
  text-align: center;
}

h1.custom-title {
  font-size: 3rem; /* 48px */
  font-weight: bold;
}

p.custom-subtitle {
  font-size: 1.5rem;
  font-weight: normal;
  color: #555;
  margin-top: 10px;
  margin-bottom: 60px;
}

.hero-header {
  margin-top: 0px;
  margin-bottom: 40px;
}

.green {
  color: #00A652;
}

.blue {
  color: #0033A0;
}
</style>
