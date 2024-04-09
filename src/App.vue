<script setup>
import { ref } from 'vue';

const title = ref('상품목록..');
const products_simple = ref(['애플', '아이폰', '아이페드', '에어팟', '맥북']);
const products = ref([
  {
    productId: '0001',
    title: 'iPhone1',
    price: 1200,
    discountRate: 15,
    isRocket: true
  },
  {
    productId: '0002',
    title: 'iPhone2',
    price: 1300,
    discountRate: 10,
    isRocket: false
  },
  {
    productId: '0023',
    title: 'iPhone3',
    price: 1400,
    discountRate: 8,
    isRocket: true
  },
  {
    productId: '0035',
    title: 'iPhone4',
    price: 1500,
    discountRate: 5,
    isRocket: false
  },
]);
const copyright = ref('Copyright 2024 Vue.js');
const imgSrc = 'https://w7.pngwing.com/pngs/854/555/png-transparent-vue-js-hd-logo-thumbnail.png'
const imgWidth = 50;

function buttonClicked() {
  alert('hi button clicked..');
}
function greetButtonClicked() {
  console.log(copyright.value);
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
  <li v-for="product in products">
    {{ product.title}} -
    ${{ product.price}}
    ({{ product.price - (product.price * (product.discountRate / 100)) }}) :
    {{ product.isRocket ? '로켓배송' : '3일후 받아요'}}
  </li>
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
