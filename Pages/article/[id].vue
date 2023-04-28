<template>
    <main>
    <Article :article="dataArticle" />
    </main>
</template>

<script setup>

const route = useRoute();
const {data:dataArticle}= await useFetch('https://fakestoreapi.com/products/'+ route.params.id);

// id c'est nom du fichier/ c'est comme il est nommé comme nom du fichier
</script>