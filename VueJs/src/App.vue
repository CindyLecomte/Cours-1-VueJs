<template>

<HelloWorld :user="user" /> <!--On passe à notre composant notre nouvelle variable, user-->

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
