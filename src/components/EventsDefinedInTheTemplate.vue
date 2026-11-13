<script setup lang="ts">
import { ref } from 'vue'

const query = ref<string>('')

// El evento nativo se tipa con Event y se obtiene el target como HTMLInputElement
const onInput = (event: Event): void => {
  const target = event.target as HTMLInputElement
  query.value = target.value
}
</script>

<template>
  <label for="query">Buscar:</label>
  <input id="query" type="text" :value="query" @input="onInput" />
  <p>Buscando:{{ query }}</p>
</template>
