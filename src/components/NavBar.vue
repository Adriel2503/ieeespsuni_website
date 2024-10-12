<template>
  <!-- Drawer para pantallas pequeñas -->
  <v-navigation-drawer
    v-model="drawer"
    app
    temporary
    class="drawer"
  >
    <v-list>
      <v-list-item
        link
        to="/"
        prepend-icon="mdi-home"
        title="Home"
        class="drawer-item"
        :class="{ 'active-tab': tab === '/' }"
      ></v-list-item>

      <v-list-item
        link
        to="/about"
        prepend-icon="mdi-information"
        title="About"
        class="drawer-item"
        :class="{ 'active-tab': tab === '/about' }"
      ></v-list-item>

      <v-list-item
        link
        to="/faq"
        prepend-icon="mdi-help-circle"
        title="FAQ"
        class="drawer-item"
        :class="{ 'active-tab': tab === '/faq' }"
      ></v-list-item>

      <!-- Botón para alternar entre modo claro y oscuro en el drawer -->
      <v-list-item
        @click="toggleDarkMode"
        :prepend-icon="isDark ? 'mdi-weather-sunny' : 'mdi-weather-night'"
        :title="isDark ? 'Modo Claro' : 'Modo Oscuro'"
        class="drawer-item"
      ></v-list-item>
    </v-list>
  </v-navigation-drawer>

  <v-app-bar app>
    <!-- Ícono de hamburguesa solo visible en pantallas pequeñas -->
    <v-app-bar-nav-icon
      @click="drawer = !drawer"
      aria-label="Open navigation menu"
      class="d-md-none"
    />

    <!-- Título alineado al lado del ícono de hamburguesa -->
    <v-toolbar-title class="titles">
      <img :src="logo" alt="IEEE SPS UNI" class="logo-svg" />
    </v-toolbar-title>

    <v-spacer></v-spacer>

    <!-- Tabs de navegación visibles solo en pantallas medianas y grandes -->
    <v-tabs
      v-model="tab"
      align-tabs="center"
      color="teal"
      class="d-none d-md-flex navigation-tabs"
    >
      <v-tab to="/" exact>
        <v-icon left>mdi-home</v-icon> Home
      </v-tab>
      <v-tab to="/about">
        <v-icon left>mdi-information</v-icon> About
      </v-tab>
      <v-tab to="/faq">
        <v-icon left>mdi-help-circle</v-icon> FAQ
      </v-tab>
    </v-tabs>

    <!-- Botón para alternar entre modo claro y oscuro en la barra -->
    <v-btn icon @click="toggleDarkMode">
      <v-icon>{{ isDark ? 'mdi-weather-sunny' : 'mdi-weather-night' }}</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script setup>
// Importar el logo SVG desde la carpeta assets
import logo from '@/assets/logo.svg'; // Ruta al logo
import { ref, watch } from 'vue';
import { useTheme } from 'vuetify';

const drawer = ref(false);
const tab = ref(null); // Control para las tabs

// Obtener el tema actual usando la API de Vuetify
const theme = useTheme();
const isDark = ref(theme.global.name.value === 'dark');

// Función para alternar entre modo oscuro y claro
const toggleDarkMode = () => {
  theme.global.name.value = isDark.value ? 'light' : 'dark'; // Alterna entre light y dark
  isDark.value = !isDark.value; // Actualiza el estado del tema
};

// Asegurarse de que el tema actualice correctamente si cambia externamente
watch(
  () => theme.global.name.value,
  (newTheme) => {
    isDark.value = newTheme === 'dark';
  }
);
</script>

<style scoped>
/* Estilos para el título */
.titles {
  display: flex;
  align-items: center; /* Centrar verticalmente */
  padding-left: 16px; /* Ajustar el espaciado según necesidad */
  height: 100%; /* Asegurar que el contenedor ocupa toda la altura */
}

/* Estilos para el logo */
.logo-svg {
  height: 50px; /* Ajusta el tamaño según necesites */
  width: auto; /* Mantener la proporción del logo */
  max-height: 100%; /* Asegurar que no se desborde en la barra */
  margin: 0; /* Eliminar márgenes */
  padding: 0; /* Eliminar padding */
  display: block; /* Asegurar que la imagen se comporte como un bloque */
}

/* Ajustes en la altura del v-app-bar */
.v-app-bar {
  height: 64px; /* Ajusta la altura para que haya espacio para el logo */
  display: flex;
  align-items: center;
  background-color: transparent; /* Asegúrate de que el fondo sea transparente */
  z-index: 1; /* Asegurar que el app-bar tenga un z-index bajo */
}

/* Ajustar para pantallas pequeñas */
@media (max-width: 600px) {
  .logo-svg {
    max-width: 135px; /* Ajusta el tamaño máximo del logo para pantallas pequeñas */
    height: 80px; /* Ajustar para pantallas más pequeñas */
  }

  .v-app-bar {
    padding: 8px;
    height: auto; /* Permitir que el app-bar sea más flexible */
  }
}

/* Personalización del Drawer */
.drawer {
  z-index: 2; /* Asegurar que el drawer se muestre sobre el app-bar */
}

/* Fondo teal para el elemento activo */
.drawer-item.v-list-item--active,
.active-tab {
  background-color: rgba(0, 121, 107, 0.1);
  color: #00796b;
}

.drawer-item.v-list-item--active .v-icon,
.active-tab .v-icon {
  color: #00796b;
}

/* Estilo en hover */
.drawer-item:hover {
  background-color: rgba(0, 121, 107, 0.1);
  color: #00796b;
}

/* Estilos del ícono cuando se hace hover o está activo */
.drawer-item:hover .v-icon,
.drawer-item.v-list-item--active .v-icon,
.active-tab .v-icon {
  color: #00796b;
}

/* Estilo del texto en el estado hover o activo */
.drawer-item:hover .v-list-item-title,
.drawer-item.v-list-item--active .v-list-item-title,
.active-tab .v-list-item-title {
  color: #00796b;
}

/* Estilo en modo oscuro */
body.theme--dark .drawer-item.v-list-item--active,
body.theme--dark .active-tab {
  background-color: rgba(255, 255, 255, 0.1);
  color: white;
}

body.theme--dark .drawer-item.v-list-item--active .v-icon,
body.theme--dark .active-tab .v-icon {
  color: white;
}
</style>
