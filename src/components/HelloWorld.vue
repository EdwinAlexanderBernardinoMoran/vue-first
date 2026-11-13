<script setup lang="ts">
import { ref } from 'vue'

import GreetingCard from './GreetingCard.vue'
import TemplateSyntax from './TemplateSyntax.vue'
import EventsDefinedInTheTemplate from './EventsDefinedInTheTemplate.vue'

const message = ref<string>('Welcome to Vue 3!')
</script>

<template>
  <p>{{ message.toUpperCase() }}</p>
  <GreetingCard />
  <TemplateSyntax />
  <EventsDefinedInTheTemplate />
</template>
