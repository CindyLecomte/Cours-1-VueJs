<template>

<h1>Hello World</h1>
<p>{{ props.subTitle }}</p> <!--On définit dans un paragraphe notre variable props, qui définit les propriétés de subTitle, et subTitle qui est 'Bonjour!'-->


</template>

<script setup>

const props = defineProps(['subTitle']); // On crée une nouvelle constante, qu'on appelle props. On utilise la méthode defineProps, qui prend un tableau, dans lequel on va indiquer le nom de notre constante, subTitle. 

</script>