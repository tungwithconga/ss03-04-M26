<template>
 <div>
  <button v-on:click="handleClick">Click me</button>
  <button v-on:click="handleDelete(1)">Delete</button>
  <button @click="handleGetEvent">EventInfo</button>
  <form @submit.prevent="handleSubmit">
    <button type="submit">Submit</button>
  </form>
  <button @keydown.esc="handleCloseForm">Dong form</button>
 </div>
</template>

<script setup>
const handleClick = () =>{
    console.log('Button clicked!')
  
};
const handleDelete = (id) =>{
    console.log(`ID`,id)
};
const handleGetEvent = (event) =>{
 console.log(`Event`,event);
};
const handleSubmit = () =>{
    alert(`Submit`);
};
const handleCloseForm = () => {
  alert ('Form closed');
};
</script>

<style>

</style>