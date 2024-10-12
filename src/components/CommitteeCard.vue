<template>
    <v-card outlined hover class="committee-card">
      <v-card-title class="text-center font-weight-bold" style="white-space: normal;">
        {{ title }}
      </v-card-title>
      <v-card-text class="text-justify">
        {{ description }}
      </v-card-text>
    </v-card>
  </template>
  
  <script>
  export default {
    props: {
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      }
    }
  };
  </script>
  
  <style scoped>
  .committee-card {
    padding: 1.25rem; /* pa-5 */
    margin: 0 auto; /* mx-auto */
    min-height: 350px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  </style>
  