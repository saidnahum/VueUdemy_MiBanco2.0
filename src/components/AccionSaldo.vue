<template>
   <button  class="font-bold" @click="accion" :disabled="desactivar">{{ texto }}</button>
</template>

<script>
export default {
   props: {
      texto: String,
      desactivar: {
         type: Boolean,
         default: false
      }
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