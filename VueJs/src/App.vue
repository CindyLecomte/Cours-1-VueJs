<template>

<HelloWorld :sub-title="subTitle" /> <!--On passe notre variable au composant parent, avec uns syntaxe en kebab-case.-->



</template>


<script setup>

import HelloWorld from './components/HelloWorld.vue'; // On importe notre composant HelloWorld



const subTitle = "Bonjour ! " // On crée une variable appelée subTitle, dans laquelle on indique le contenu qu'on veut.

</script>





<style scoped>

</style>
