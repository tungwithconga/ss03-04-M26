<template>
  <div :class="[isActive ? 'active' : '', 'block']" :style="{ backgroundColor }">
    Block
  </div>
  <p>isActive={{ isActive }}</p>
</template>

<script setup>
import { ref } from 'vue';

const isActive = ref(true);
const backgroundColor = ref('blue');
</script>

<style scoped>
.block {
  width: 200px;
  height: 100px;
  text-align: center;
  color: white;
  line-height: 100px;
}

.active {
  color: #fff;
}
</style>
