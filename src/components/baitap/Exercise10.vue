<template>
  <div>
    <input v-model="inputValue" placeholder="Nhập giá trị" />
  </div>
</template>

<script setup>
import { ref, watch } from 'vue';

const inputValue = ref('');

watch(inputValue, (newValue, oldValue) => {
  console.log(`Giá trị thay đổi từ "${oldValue}" thành "${newValue}"`);
});
</script>

<style scoped>

</style>
