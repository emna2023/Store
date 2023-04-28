<template>
    <article :article="dataArticle"></article>
</template>

<script setup>

const route = useRoute();
const {data:dataArticle}= await useFetch('https://fakestoreapi.com/products/'+ route.params.id);
</script>