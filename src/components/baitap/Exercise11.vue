<template>
  <div>
    <h1>Giỏ hàng</h1>
    <ul>
      <li v-for="(item, index) in cartItems" :key="index">
        {{ item.name }} - Số lượng: {{ item.quantity }}
        <button @click="increaseQuantity(index)">Tăng số lượng</button>
      </li>
    </ul>
    <p>Tổng số lượng sản phẩm: {{ totalQuantity }}</p>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const cartItems = ref([
  { name: 'Mền Mền Loại 1', quantity: 3 },
  { name: 'Mền Mền Loại 2', quantity: 5 },
  { name: 'Mền Mền Loại 3', quantity: 1 }
]);

const increaseQuantity = (index) => {
  cartItems.value[index].quantity += 1;
};

const totalQuantity = computed(() => {
  return cartItems.value.reduce((total, item) => total + item.quantity, 0);
});
</script>

<style scoped>
button {
  margin-left: 10px;
  padding: 5px 10px;
  color: white;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}
</style>
