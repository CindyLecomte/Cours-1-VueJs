<template>

<HelloWorld :sub-title="subTitle" /> <!--On passe notre variable au composant parent, avec uns syntaxe en kebab-case.-->

<input type="text" v-model="subTitle"> <!--On crée un input texte. On lie la variable à l'input avec v-model. Cela permet de lier un input à une variable. -->

</template>


<script setup>

import HelloWorld from './components/HelloWorld.vue'; // On importe notre composant HelloWorld
import { ref } from 'vue';


const subTitle = ref(""); // On définit que notre variable subTitle utilise ref. Ce qui va faire en sorte qu'au changement dans l'input, la valeur va changer. On met une chaîne de caractère vide par défaut, mais si on change la valeur dans le navigateur, cela fonctionnera.



</script>





<style scoped>

</style>
