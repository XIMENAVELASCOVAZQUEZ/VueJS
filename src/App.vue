<script setup>
const name = "Vue dinámico";
const activo = false
const arrayFrutas = [
  {
    name: "Manzana",
    price: "$1.00",
    description: "Una manzana",
    stock: 0,
  },
  {
    name: "Pera",
    price: "$2.00",
    description: "Una pera",
    stock: 10,
  },
  {
    name: "Naranja",
    price: "$3.00",
    description: "Una naranja",
    stock: 20,
  },
];

</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <ui>
    <li v-if="item.stock > 0" v-for="item in arrayFrutas" :key="item.name">
      {{ item.name }} - {{ item.price }}
    </li>
  </ui>
</template>


<style>
h1 {
  color: rgb(234, 0, 255);
}
</style>