<script setup>
import { ref, watch } from 'vue'

const props = defineProps({
  modelValue: String,
  type: String,
})

const emit = defineEmits(['update:modelValue'])

const value = ref(props.modelValue)

watch(value, (newVal) => {
  emit('update:modelValue', newVal)
})
</script>

<template>
  <div class="child">
    <input v-model="value" :type="props.type" />
    <p>This is the child component.</p>
  </div>
</template>

<style scoped>
.child {
  padding: 1em;
  border: 1px solid skyblue;
  width: 50%;
}
</style>
