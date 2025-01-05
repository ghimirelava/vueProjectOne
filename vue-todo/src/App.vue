<template>
  <h1 @click="handleHeadingClick"> My name is {{ name }}, I am {{ age }} years old.</h1>
</template>

<!-- script setup pattern example -->
<script setup>

//ref function that creates a reactive reference to a val
import { ref } from 'vue'

const name = ref('Lava')
const age = ref(24)

//method changes the ref vals updating the template
const handleHeadingClick = () => {
  name.value = 'Steve'
  age.value = 27
}
</script>