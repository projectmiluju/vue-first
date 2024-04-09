<script setup>
import { ref } from 'vue';

const title = ref('상품목록..');
const products = ref(['애플', '아이폰', '아이페드', '에어팟', '맥북']);
const copyright = ref('Copyright 2024 Vue.js');
const imgSrc = 'https://w7.pngwing.com/pngs/854/555/png-transparent-vue-js-hd-logo-thumbnail.png'
const imgWidth = 50;

function buttonClicked() {
  alert('hi button clicked..');
}
function greetButtonClicked() {
  console.log('hi');
}
</script>

<template>

<h1>Hi Vue</h1>
<hr>
<img :src="imgSrc" :width="imgWidth">
<button @click="buttonClicked">Click!</button>
<button @click="greetButtonClicked">누르면 콘솔로 인사를 합니다.</button>
<h3>{{ title }}</h3>
<ul>
  <li v-for="product in products">{{ product }}</li>
</ul>
<h3>{{ copyright }}</h3>

</template>

<style scoped>
h1 {
  color: brown;
}
h3 {
  color: rebeccapurple;
}
</style>
