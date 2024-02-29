<script setup>

import { ref , computed} from "vue";

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

const classCounter = () => {
  if(counter.value === 0){
    return 'zero'
  }
  if(counter.value > 0) {
    return 'positive'
  }
  if(counter.value < 0) {
    return 'negative'
  }
};
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <h2 :class="classCounter()">{{ counter }}</h2>
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

.zero {
  color:blueviolet;
}
</style>