<template>
<div>
  <img v-bind:src="url" alt="">
  <!-- <img :src="url" alt=""> -->
  <button :disabled="isDisabled">Click me</button>
  <!-- Khi o trong su dung gia tri nhu la disabled thi dung : -->
  <input type="text" :disabled="isDisabledInput">
  <div v-bind="divAtributes">Container</div>
  <!-- khi co 2 thuoc tinh tro len su dung "=" thay vi ":" -->
  <p>Nội dung</p>
  <div v-bind:class="{textRed:isTextRed}">Hello world</div>
  </div>

</template>

<script setup>
const url = "https://media-cdn.tripadvisor.com/media/attractions-splice-spp-674x446/0c/04/55/9b.jpg";

const isDisabled = false;

const isDisabledInput = true;

const divAtributes = {
  id:"container",
  class: "container",
};

const paragraphAttributes = {
  id: "paragraph",
  class: "paragraph",
};

const isTextRed = true;
</script>

<style>
.textRed{
  color: red;
}

</style>