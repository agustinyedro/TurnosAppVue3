<template>
  <v-app>
    <!-- Mostrar NavBar solo si hay sesión activa -->
    <NavBar v-if="isAuthenticated" />

    <!-- Contenido principal -->
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts" setup>
import NavBar from './components/sidebar/NavBar.vue'
import { useAuth } from './composables/useAuth.ts'

const { isAuthenticated } = useAuth()
</script>

<style>
body {
  font-family: 'Roboto Flex', sans-serif;
}
</style>
