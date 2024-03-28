<template>

<h1>Hello World</h1>

{{ name }} <!--On affiche name-->

<input type="text" v-model="name" @input="handleUpdate"> <!--On crée un input qu'on lie à name. A cet input, on lie un événement. Au changement de cet input, on va appeler handleUpdate.-->

</template>

<script setup>

import{ ref } from 'vue'; //On importe ici ref depuis vue

const emit = defineEmits(['updateName']); //On crée une const emit, à laquelle on va utiliser definEmit, qui va prendre ce qu'on va appeler updateName.

const handleUpdate = (event) => {
   emit('updateName', event.target.value);  //On va utiliser emit. On lui donne le nom de l'événement (updateName), et on va lui passer la valeur qu'on avait avant dans le console.log
}


const name = ref(""); //On crée une const name, qui sera une chaîne de caractère vide par défaut.

</script>