<script setup>
  const name = 'Vue dinámico';
  const arrayFrutas = ["🍎", "🍌", "🍉", "🍓", "🍒"];
</script>


<template> 
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <ui>
    <li
      v-for="(fruta, index) in arrayFrutas"
      :key="index"
      >{{ index }} - {{ fruta }}
  </li>
  </ui>
</template>


<style>
  h1 {
    color: rgb(234, 0, 255);
  }
</style>