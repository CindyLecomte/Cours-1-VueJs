<template>

<HelloWorld /> 


<input type="text" v-model="name">
<input type="text" v-model="age">     

</template>


<script setup>

import HelloWorld from './components/HelloWorld.vue'; // On importe notre composant HelloWorld
import { watch, ref } from 'vue'; //On importe ref et watch



const name = ref('Cindy');
const age = ref(26);    //On crée deux variable avec le nom et l'âge


watch(name, (newValue, oldValue) => { //On crée un watch qui prend le name. Il prend en paramètre une nouvelle valeur et une ancienne valeur. On va lui passer un callback, qui va rendre un console.log de la nouvelle valeur, et de l'ancienne valeur. 
    console.log(newValue, oldValue) // Lorsqu'on va regarder en console, au changement de l'input name, on aura bien la nouvelle valeur suivi de l'ancienne valeur.
})

</script>



<style scoped>


</style>
