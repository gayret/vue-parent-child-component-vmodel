<script setup>
import { ref } from 'vue'
import Child from './components/Child.vue'

const someThing = ref('Hello')
</script>

<template>
  <div class="parent">
    <h1>{{ someThing }}</h1>
    <p>This is the parent component.</p>
  </div>
  <child v-model="someThing" type="text" />
</template>

<style scoped>
.parent {
  padding: 1em;
  border: 1px solid green;
}
</style>
