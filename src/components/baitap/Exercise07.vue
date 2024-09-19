<template>
  <div>
    <button @click="count++">Click {{ count }} lần</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);
</script>

<style scoped>

</style>
