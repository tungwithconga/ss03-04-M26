<template>
  <button v-on:click="handleClick">Click me</button>
</template>

<script setup>
const handleClick = () =>{
    console.log('clicked!')
  
};
</script>

<style>

</style>