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



</script>





<style scoped>

</style>
