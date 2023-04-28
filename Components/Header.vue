<template>
<header class="bg-red-700 bg-amber-300 text-2xl content-center">
<h1>Le header</h1>
<NuxtLink :to="'/category/index.vue'">
    <h1 class="font-medium font-mono bg-yellow-800 border-orange-900">Listes des catégories</h1>
</NuxtLink>

</header>
</template>

<script setup>
</script>
<style scoped>
h1{
    text-align: center;
}
</style>