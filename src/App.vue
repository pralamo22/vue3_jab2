<template>
  <div class="text-center">
    <h1> ****** EMITS *******</h1>
    <br>
    <h2>Soy el padre</h2>
    <HijoVue1 :nombre="nombre" :edad="edad" @modificar="cambiarValor" />
  </div>

  <br>
  <br>
  <div class="text-center">
    <h1> ****** INYECCION *******</h1>
    <br>
    <h2>Soy el padre</h2>
    <HijoVue2 :nombre="nombre" :edad="edad" @modificar="cambiarValor" />
  </div>
</template>

<script setup>
  import { ref, provide } from 'vue';
  import HijoVue1 from './components/Hijo1.vue';
  import HijoVue2 from './components/Hijo2.vue';
  const nombre = ref('Pablo');
  const edad = ref('50');
  const canal = ref("Pralamo");
  provide('miCanal', canal);
  const cambiarValor = (valor1, valor2) => {
    nombre.value = valor1;
    edad.value = valor2;

  }

</script>

<style lang="css" scoped></style>