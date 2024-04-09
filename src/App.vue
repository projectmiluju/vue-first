<script setup>
import { ref } from 'vue';

const title = ref('상품목록..');
const products = ref(['애플', '아이폰', '아이페드', '에어팟']);
const copyright = ref('Copyright 2024 Vue.js');
const imgSrc = 'https://w7.pngwing.com/pngs/854/555/png-transparent-vue-js-hd-logo-thumbnail.png'
const imgWidth = 500;
</script>

<template>

<h1>Hi Vue</h1>
<hr>
<img :src="imgSrc" :width="imgWidth">
<h3>{{ title }}</h3>
<ul>
  <li>{{ products[0] }}</li>
  <li>{{ products[1] }}</li>
  <li>{{ products[2] }}</li>
  <li>{{ products[3] }}</li>
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
