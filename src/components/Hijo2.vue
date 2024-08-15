<template>
  <div>
    <h1>Soy el hijo2</h1>
    <h2>{{ canal }}</h2>
    <button @click="modificar">Cambiar</button>
  </div>
</template>

<script setup>
import { inject } from "vue";

const canal = inject("miCanal");

const modificar = () => {
  canal.value = "nuevo pralamo a través del canal";
};
</script>

<style lang="css" scoped></style>
