<!-- File contains pratice cod eto understand core vue concepts -->
<template>
  <h1 @click="handleHeadingClick"> My name is {{ name }}, I am {{ age }} years old.</h1>
  <MyButton 
    @buttonClicked = "ShowAlert"
    title = "My Button Title"
  />
</template>

<!-- script setup pattern example -->
<script setup>

//ref function that creates a reactive reference to a val
import { ref } from 'vue'

//importing a child component from components files
import MyButton from '@/components/MyButton.vue'

const name = ref('Lava')
const age = ref(24)

//method changes the ref vals updating the template
const handleHeadingClick = () => {
  name.value = 'Steve'
  age.value = 27
}

const ShowAlert = newAge => {
  //alert('Child button was clicked!')
  age.value = newAge
}
</script>