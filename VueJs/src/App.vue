<template>

<HelloWorld :name="name" :age="age" /> <!--On passe à notre composant les variables name et age-->

<input type="text" v-model="name"> <!--On crée un input qu'on relie à la variable name grâce à v-model-->
<input type="text" v-model="age">   <!--On crée un input qu'on relie à la variable age frâce à v-model-->

</template>


<script setup>

import HelloWorld from './components/HelloWorld.vue'; // On importe notre composant HelloWorld
import { ref } from 'vue';

const name = ref("Cindy"); //On crée une variable contenant le nom
const age = ref(26); // Et une variable contenant l'âge


const display = () => {
    console.log(name.value, age.value) // On crée une  fonction qui va simplement faire un affichage en console, grâce au .value 
}

display() // On appelle notre fonction

</script>





<style scoped>

</style>
