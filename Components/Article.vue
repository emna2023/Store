<template>

<ul p-10  m-8>
    <li> 
        <List v-for="(info,cle) in article"
        :contenu="info" :titre="cle" />
    </li>
</ul>

</template>


<script setup>
const props=defineProps({

    article: Object,
});


</script>