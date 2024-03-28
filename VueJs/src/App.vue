<template>

<HelloWorld

@update-name="name => display(name)" 
/>  <!--On va écouter l'événement depuis ce composant, le composant parent. On fait un @update-name, et on lui passe les arguments : le name, qu'on va envoyer dans la fonction que l'on veut (display(name))-->

</template>


<script setup>

import HelloWorld from './components/HelloWorld.vue'; // On importe notre composant HelloWorld

const display = (name) => {
    console.log('App.vue : ' + name)    // Le name mis à jour, on va le console.log : On crée une const display, qui est une fonction, qui prend le name mis à jour. On fait ensuite un console.log depuis App.vue et on console.log notre name.
}

</script>



<style scoped>


</style>
