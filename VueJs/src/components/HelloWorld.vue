<template>

<h1>Hello World</h1>
<p>{{ props.name }} {{ props.age }}</p> <!--On affiche ici le nom et l'âge grâce aux props-->


</template>

<script setup>

const props = defineProps(['name', 'age']); // On change defineProps en lui passant name et age

</script>