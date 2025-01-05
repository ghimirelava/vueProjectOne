<template>
    
    <button @click = "$emit('buttonClicked')"> {{ props.title }} </button>
</template>

<script setup>

//defineProps function does not need to be imported
//defines the title of the button
const props = defineProps({
    title:{
        type: String,
        default: "No title added"
    }
}) 

const emit = defineEmits(['busttonClicked'])

//must use props.title to acces the prop in script
console.log(props.title)
</script>