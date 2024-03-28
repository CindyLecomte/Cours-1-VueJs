<template>

<HelloWorld /> 


<div
:class="[user.age > 30 ? 'text-red' : 'text-green']"
>   <!--On attribue une class à cette div en faisant une condition en ternaire : si l'âge de l'utilisateur est strictement supérieur à 30, le nom sera en rouge. Sinon, le nom sera en vert. Cela changera si on change l'âge dans notre const user.-->

    {{ user.name }} <!--On crée une div dans laquelle on va afficher le nom du user-->

</div>


</template>


<script setup>

import HelloWorld from './components/HelloWorld.vue'; // On importe notre composant HelloWorld
import { reactive } from 'vue'; //On importe reactive

const user = reactive ({ // Au lieu de ref, on met reactive
    name : 'Cindy',
    age: 31,    // On crée une nouvelle constante en lui passant un objet, avec le name et l'age.
})



</script>





<style scoped>

.text-red {
    color: red;
}

.text-green {
    color: green; /* On crée une classe pour une couleur rouge et une classe pour la couleur verte*/
}

</style>
