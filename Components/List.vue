<template>



<div v-if="titre==='rating'" 
ratingcontenu="contenu" ratingtitre="titre" >
  </div>
<div v-else-if="titre==='image'" >
  <img class="w-72" alt="new image" :src="contenu" />
  <strong> {{'ratingtitre'}} : {{ ratingcontenu }}</strong> <br/>


<NuxtLink to:="'article/' + 'titre'">
    <button class="bouton">voir l'article</button>
</NuxtLink>
</div>
<div v-else>
<strong>{{ titre }} : {{ contenu }}</strong> 
</div>


</template>


<script setup>
const route = useRoute();
let ratingcontenu;
let ratingtitre;

const props= defineProps({

contenu: [Object, String, Number],
titre:String,

});

</script>
<style scoped>
.bouton{
    text-align: center;
    color:blue
    
}

</style>