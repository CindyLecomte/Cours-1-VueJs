<template>

<HelloWorld :user="user" /> <!--On passe à notre composant notre nouvelle variable, user-->



<input type="text" v-model="user.name" v-on:input="display"> <!--On peut greffer des choses au niveau des événements. On utilise v-on sur input du name. -->
<input type="text" v-model="user.age">  <!--Et un qui va être lié a age. On doit mettre user. devant, car c'est un objet.-->


</template>


<script setup>

import HelloWorld from './components/HelloWorld.vue'; // On importe notre composant HelloWorld
import { reactive } from 'vue'; //On importe reactive

const user = reactive ({ // Au lieu de ref, on met reactive
    name : 'Cindy',
    age: 26,    // On crée une nouvelle constante en lui passant un objet, avec le name et l'age.
})

const display = () => { 
    console.log(user.name, user.age); // On crée une fonction display, où on va afficher en console le nom et l'âge. Puisqu'on a mis v-on sur le name, on aura un changement en console à chaque modification de l'input name. (mais pas de l'âge)
}

display() //On oublie pas d'appeler la fonction

</script>





<style scoped>

</style>
