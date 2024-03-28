<template>

<HelloWorld /> 

<span>{{ sentence }}</span> <!--On remplace la phrase qu'on avait auparavant, par celle qu'on a définit avec la méthode computed.-->
<br><br>
<input type="text" v-model="name">
<input type="text" v-model="age">      <!--On crée deux input pour pouvoir changer les données par le formulaire.-->

</template>


<script setup>

import HelloWorld from './components/HelloWorld.vue'; // On importe notre composant HelloWorld
import { computed, ref } from 'vue'; //On importe ref et computed


const sentence = computed (() => {
    return `Bonjour, je m'appelle ${name.value} et j'ai ${age.value}` // On crée une variable appelée sentence, qui va utiliser la méthode computed. On va retourner une phrase qui prend en compte les deux variables. 
})

const name = ref('Cindy');

const age = ref(26);    //On crée deux variable avec le nom et l'âge

</script>



<style scoped>


</style>
