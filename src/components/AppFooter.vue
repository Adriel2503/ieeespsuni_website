<template>
  <v-footer height="40" app class="footer-with-line">
    <!-- Enlaces a redes sociales -->
    <a
      v-for="item in items"
      :key="item.title"
      :href="item.href"
      :title="item.title"
      class="d-inline-block mx-2 social-link"
      rel="noopener noreferrer"
      target="_blank"
    >
      <v-icon
        :icon="item.icon"
        :size="item.icon === '$vuetify' ? 24 : 16"
      />
    </a>

    <!-- Derechos de autor -->
    <div
      class="text-caption text-disabled"
      style="position: absolute; right: 16px;"
    >
      &copy; 2016-{{ new Date().getFullYear() }} <span class="d-none d-sm-inline-block">IEEE SPS UNI</span>
      —
      <a
        class="text-decoration-none on-surface"
        href="https://ieeespsuni.com/licensing"
        rel="noopener noreferrer"
        target="_blank"
      >
        MIT License
      </a>
    </div>
  </v-footer>
</template>

<script setup>
const items = [
  {
    title: 'Facebook',
    icon: 'mdi-facebook',
    href: 'https://facebook.com/ieeespsuni', // Cambiar al enlace real de IEEE SPS UNI
  },
  {
    title: 'LinkedIn',
    icon: 'mdi-linkedin',
    href: 'https://www.linkedin.com/company/ieee-sps-uni/', // Cambiar al enlace real
  },
  {
    title: 'Instagram',
    icon: 'mdi-instagram',
    href: 'https://instagram.com/ieee_sps_uni', // Cambiar al enlace real
  },
  {
    title: 'GitHub',
    icon: 'mdi-github',
    href: 'https://github.com', // Cambiar al enlace real si aplica
  },
];
</script>

<style scoped lang="sass">
.footer-with-line
  border-top: 1px solid rgba(0, 0, 0, 0.12) // Línea en la parte superior del footer
  padding-top: 8px // Añadir espacio entre la línea y el contenido

.social-link :deep(.v-icon)
  color: rgba(var(--v-theme-on-background), var(--v-disabled-opacity))
  text-decoration: none
  transition: .2s ease-in-out

  &:hover
    color: rgba(25, 118, 210, 1) // Color de hover azul
</style>
