<template>

   <button 
      class="bg-green-500 hover:bg-green-600 p-2 rounded text-white m-2"
      @click="accion"

   >{{ texto }}</button>
</template>

<script>
export default {
   props: {
      texto: String
   },
   data() {
      return {
         color: true
      }
   },
   methods: {
      accion(){
         this.$emit('action')
      }
   }
}
</script>

<style>

</style>