<template>
<strong>Liste des catégories</strong>
   <ul>
    <li v-for="category in categories">
        <NuxtLink to="">
    {{ category }}
</NuxtLink>
    </li>
   </ul> 
    
</template>

<script setup>


    const {data:categories}= await usefatch('https://fakestoreapi.com/products/categories');
    

</script>