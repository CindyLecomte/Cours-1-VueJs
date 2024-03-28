<template>

<h1>Hello World</h1>

{{ name }} <!--On affiche name-->

<input type="text" v-model="name" @input="handleUpdate"> <!--On crée un input qu'on lie à name. A cet input, on lie un événement. Au changement de cet input, on va appeler handleUpdate.-->

</template>

<script setup>

import{ ref } from 'vue'; //On importe ici ref depuis vue

const handleUpdate = (event) => {
    console.log(event.target.value) // On crée la fonction handleUpdate, qui va récupérer l'événement. On fait un console.log de l'event, et on récupère la valeur de l'input. De cette manière, on aura la valeur de l'input en console.
};



const emit = defineEmits(['updateName']); //On crée une const emit, à laquelle on va utiliser definEmit, qui va prendre ce qu'on va appeler updateName.

const name = ref(""); //On crée une const name, qui sera une chaîne de caractère vide par défaut.

</script>