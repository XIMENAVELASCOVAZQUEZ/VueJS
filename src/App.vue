<script setup>

import { ref } from "vue";

const name = "Vue dinámico";

const counter = ref(0);

const increment = () => {
  counter.value++;
};

const decrement = () => {
  counter.value--;
};

const reset = () => {
  counter.value=0;
};
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <h2 :class="counter > 0 ? 'positive' : 'negative' ">{{ counter }}</h2>
  <button @click="increment">Aumentar</button>
  <button @click="decrement">Disminuir</button>
  <button @click="reset">Reset</button>
</template>

<style>
h1 {
  color: rgb(234, 0, 255);
}

.positive {
  color: green;
}

.negative {
  color: red;
}
</style>