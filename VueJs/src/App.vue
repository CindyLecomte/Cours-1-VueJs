<template>

<HelloWorld :user="user" /> <!--On passe à notre composant notre nouvelle variable, user-->


<div

v-if="user.age > 15" 
> <!--On crée une condition avec v-if : si user.age est strictement supérieur à 15, Mon âge sera afifché. -->
Mon âge <!--On crée une div dans laquelle on inscrit Mon âge-->

</div>


<input type="text" v-model="user.name"> <!--On crée deux nouveaux inpout, un qui va être lié au name-->
<input type="text" v-model="user.age">  <!--Et un qui va être lié a age. On doit mettre user. devant, car c'est un objet.-->


</template>


<script setup>

import HelloWorld from './components/HelloWorld.vue'; // On importe notre composant HelloWorld
import { reactive } from 'vue'; //On importe reactive

const user = reactive ({ // Au lieu de ref, on met reactive
    name : 'Cindy',
    age: 26,    // On crée une nouvelle constante en lui passant un objet, avec le name et l'age.
})

const display = () => { // On crée une fonction display, qui va afficher en console user.
    console.log(user);
}

display() //On oublie pas d'appeler la fonction

</script>





<style scoped>

</style>
