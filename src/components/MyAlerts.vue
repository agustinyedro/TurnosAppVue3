<!-- eslint-disable vue/no-mutating-props -->
<template>
  <v-snackbar v-model="alert.show" :color="alert.type" :timeout="timeout" class="mt-6 elevation-10">
    {{ alert.message }}
    <template v-slot:action="{ attrs }">
      <v-btn color="white" text v-bind="attrs" @click="cerrarSnackbar"> Cerrar </v-btn>
    </template>
  </v-snackbar>
</template>

<script lang="ts" setup>
import { defineProps, defineEmits } from 'vue'

// Definir la interfaz para la prop 'alert'
interface Alert {
  show: boolean
  type: string
  message: string
}

// Definir las propiedades
const props = defineProps<{
  alert: Alert
  timeout: number
}>()

// Emitir eventos
const emit = defineEmits<{
  (e: 'update:alert', alert: Alert): void
}>()

// Función para cerrar el snackbar
const cerrarSnackbar = () => {
  // Emitir el evento para actualizar la prop 'alert' en el componente padre
  emit('update:alert', { ...props.alert, show: false })
}
</script>
