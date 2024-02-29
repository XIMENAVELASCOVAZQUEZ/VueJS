<script setup>
const name = "Vue dinámico";
const objetoFruta = {
  name: "Manzana",
  price: "$1.00",
  description: "Una manzana",
  id: 1,
};
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  {{ objetoFruta }}
  <ui>
    <li v-for="(value, propiedad, index) in objetoFruta" :key="value">
      {{index}} - {{propiedad}} : {{ value }}
    </li>
  </ui>
</template>


<style>
h1 {
  color: rgb(234, 0, 255);
}
</style>