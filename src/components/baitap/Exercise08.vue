<template>
  <div>
    <p>Company: {{ info.company }}</p>
    <p>Age: {{ info.age }}</p>
    <button @click="changeData">Change data</button>
  </div>
</template>

<script setup>
import { reactive } from 'vue';

const info = reactive({
  company: 'Rikkei Academy',
  age: 2
});

const changeData = () => {
  info.company = 'Rikkei Education';
  info.age = 1;
};
</script>

<style scoped>
button {
  padding: 10px 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}
</style>
