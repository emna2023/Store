<template>

<!-- <ul p-10  m-8>
    <li> 
        <List v-for="(info,cle) in article"
        :contenu="info" :titre="cle" />
    </li>
</ul> --> 
 <ul>
    <li class="p-3.5" >
        <strong>{{oneProduct.title}} </strong>
    </li>
    <li class="p-3.5" v-for="(contenu,index) in dataProducts">
        <strong>{{ index }} : {{ contenu }} </strong>
    </li>
    <li>
        <img alt="emna" :src="article.image" />
     </li>
    <li> 
        <NuxtLink  v-if="routeName!='article-id'"   :to="'/article/' + oneProduct.id">
        <span class="bg-amber-300">voir les détails du produit</span>
        </NuxtLink>
    </li>


        
</ul>

  
</template>


<script setup>
const props=defineProps({

    article: Object,
});
const routeName=useRoute().name;

const oneProduct=props.article;
const dataProducts=ref('');
dataProducts.value={
'categorie':oneProduct.category,
'Description': oneProduct.description,
'Price': oneProduct.price + '$',
'Evaluation': oneProduct.rating.rate+ "/5"+
'  évalué par '+
oneProduct.rating.count + " personnes.",

                    };


</script>
<style scoped>
img{
    width:30%;
}
</style>