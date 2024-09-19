<template>
  <div>
    <input type="number" v-model.number="inputValue" />
    <button @click="addToCart">Add to cart</button>
    
    <p>Tổng tiền trong giỏ hàng: {{ totalPrice }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const inputValue = ref(0);
const totalPrice = ref(0);

const addToCart = () => {
  totalPrice.value += inputValue.value;
  inputValue.value = 0; 
};
</script>

<style scoped>
input {
  margin-right: 10px;
  padding: 5px;
}

button {
  padding: 5px 10px;
  color: white;
  border: none;
  cursor: pointer;
}
</style>
