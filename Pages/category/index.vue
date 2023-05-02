<template>
    <main>
<strong class="py-6">Liste des catégories</strong>
   <ul>
    <li v-for="category in categories">
        <NuxtLink to="'/category/'" +category>  
    {{ category }}
 </NuxtLink>  
    </li>
   </ul> 
</main>
    
</template>

<script setup>


    const {data:categories}= await useFetch('https://fakestoreapi.com/products/categories');
    console.log(categories.value);


    

</script>