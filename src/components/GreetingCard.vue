<script setup lang="ts">
import { ref } from 'vue'

const name = ref<string>('Edwin Bernardino')
</script>

<template>
  <h2 class="greeting">Hello, {{ name }}!</h2>
</template>

<style scoped>
.greeting {
  color: #42b983;
}
</style>
