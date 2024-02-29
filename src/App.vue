<script setup>
  const name = 'Vue dinámico';
  const arrayFrutas = [
        {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        },
        {
            name: "Pera",
            price: "$2.00",
            description: "Una pera",
        },
        {
            name: "Naranja",
            price: "$3.00",
            description: "Una naranja",
        },
    ];
</script>


<template> 
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <ui>
    <li
      v-for="fruta in arrayFrutas"
      :key="fruta.name"
    >
      {{ fruta.name }} - {{ fruta.price}} - {{ fruta.description }}
    </li>
  </ui>
</template>


<style>
  h1 {
    color: rgb(234, 0, 255);
  }
</style>