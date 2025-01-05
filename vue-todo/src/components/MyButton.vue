<template>
    <button> {{ title }} </button>
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
</script>