<template>
   <!-- <Navbar/> -->
   <div class="container mx-auto space-y-3">
      <div class="flex justify-center">
         <img class="w-64 mb-5" alt="Vue logo" src="./assets/logo.png" />
      </div>
      <Titulo titulo="iBanco"/>
      <Cuenta />
      
   </div>
</template>

<script>
import Titulo from "./components/Titulo";
import Cuenta from "./components/Cuenta";
import Navbar from "./components/Navbar"

export default {
   name: "App",
   components: {
      Titulo, Cuenta, Navbar
   },
};
</script>

<style>
</style>
