<template>
    
    <button @click = "handleButtonClicked"> {{ props.title }} </button>
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

const handleButtonClicked = () => {
    emit('buttonClicked', 29)
}

//must use props.title to acces the prop in script
console.log(props.title)
</script>