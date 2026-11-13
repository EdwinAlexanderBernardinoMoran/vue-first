<script setup lang="ts">
import { ref } from 'vue'

import viteLogo from '../assets/vite.svg'

const count = ref<number>(0)
const message = ref('Welcome to Vue 3!')
const isDisable = ref<boolean>(false)

const increment = () => {
  count.value++ // en <script> siempre se usa .value
}

const decrement = () => {
  if (count.value === 0) return

  count.value--
}
</script>

<template>
  <!-- Interpolación: solo admite UNA expresión de JS, no sentencias -->
  <p>{{ message.toUpperCase() }} - {{ count * 2 }}</p>

  <!-- v-bind (forma corta: ":"): enlaza un atributo a una expresión  -->
  <img :src="viteLogo" :alt="message" />
  <button :disabled="isDisable">No disponible</button>

  <!-- v-on (forma corta: "@"): escucha eventos -->
  <button @click="increment">Increment</button>
  <button @click="decrement">Decrement</button>

  <!-- Clases y estilos dinámicos (se profundiza en la sección 2) -->
  <p :class="{ negative: count < 0 }" :style="{ fontSize: 16 + count + 'px' }">{{ count }}</p>
</template>
