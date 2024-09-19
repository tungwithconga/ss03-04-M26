<template>
  <div>
    <p>Khi width={{ width }}, height={{ height }}</p>
    <p>Acreage: {{ acreage }}</p>
    <button @click="increaseWidth">Increase width</button>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const width = ref(10);
const height = ref(20);

const acreage = computed(() => width.value * height.value);

const increaseWidth = () => {
  width.value += 10;
};
</script>

<style scoped>

</style>
