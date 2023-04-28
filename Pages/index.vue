<template>
<main>
    <h1 class="font-medium font-mono bg-lime-400">Liste des articles</h1>

<Article v-for="myarticle in datastore" :article="myarticle" /> 

</main>
</template>
<script setup>

const {data:datastore}= await useFetch('https://fakestoreapi.com/products?limit=6');
console.log(datastore.value);
console.log(datastore.value[0]);



</script>