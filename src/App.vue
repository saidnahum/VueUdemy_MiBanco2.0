<template>
   <div class="container mx-auto space-y-3">
      <div class="flex justify-center">
         <img class="w-64 mb-5" alt="Vue logo" src="./assets/logo.png" />
      </div>
      <Titulo titulo="Título dinámico 2.0"/>
      <Cuenta />
   </div>
</template>

<script>
import Titulo from "./components/Titulo";
import Cuenta from "./components/Cuenta";

export default {
   name: "App",
   components: {
      Titulo, Cuenta
   },
};
</script>

<style>
</style>
