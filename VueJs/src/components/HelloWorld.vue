<template>

<h1>Hello World</h1>
<p>{{ props.user.name }} {{ props.user.age }}</p> <!--On affiche le nom de l'user ainsi que l'âge du user.-->


</template>

<script setup>

const props = defineProps(['user']); // On change defineProps, en lui passant cette fois user.

</script>