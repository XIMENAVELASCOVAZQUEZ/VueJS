<script setup>
const name = "Vue dinámico";

//metodo - methods
const handleClick = () => {
  console.log("me diste click");
};
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <button v-on:click="handleClick">Activame 1</button>
  <button @click="handleClick">Activame 2</button>
</template>

<style>
h1 {
  color: rgb(234, 0, 255);
}
</style>