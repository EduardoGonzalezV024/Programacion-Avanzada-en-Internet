<template>
  <h1>Hola {{ name }}</h1>
  <input v-model="name" />

  <br><br>
  <button @:click="count++">Contador: {{ count }}</button>

  <br><br><br><br>
  <input v-model="n1" placeholder="Numero 1"/>
  +
  <input v-model="n2" placeholder="Numero 2"/>

  <br><br>
  <button @:click="suma = (+n1) + (+n2)">Suma</button>

  <p>El resultado es: {{ suma }}</p>
</template>

<script setup>
  import { ref } from 'vue'

  const name = ref('');
  const count = ref(0);

  const n1 = ref(0);
  const n2 = ref(0);
  const suma = ref(0);
</script>

<style>
  h1 {
    color:blue;
  }
</style>
