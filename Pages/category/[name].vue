<template>


<Article v-for="item in items" :article="item"/>

</template>
<script setup>

const route= useRoute();
const categoryName= route.params.name;

const {data:items}= await useFetch('https://fakestoreapi.com/products/category/'+ categoryName);

</script>