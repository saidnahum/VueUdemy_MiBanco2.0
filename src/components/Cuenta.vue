<template>
   <div class="space-y-5">
      <h2 class="text-3xl text-center">Tipo de Cuenta: <span class="font-bold">{{ cuenta }}</span></h2>
      <h2 class="text-3xl text-center">Saldo: <span class="font-bold">{{ saldo }}</span></h2>
      <h2 class="text-3xl text-center">Cuenta: <span class="font-bold">{{ estado ? 'Activada' : 'Desactivada' }}</span></h2>
      <h2 class="text-3xl text-center">Servicios:</h2>
      <ul>
         <div class="text-center" v-for="(servicio, index) in servicios" :key="index">
            <li> {{ index +1 }}.- <span class="font-bold">{{ servicio }}</span></li>
         </div>  
      </ul>

      <div class="flex justify-center">
         <AccionSaldo 
            texto="Aumentar Saldo" 
            @action="aumentar"
         />
         <AccionSaldo 
            texto="Disminuir Saldo" 
            @action="disminuir"
         />
      </div>
      
   </div>
</template>

<script>

import AccionSaldo from './AccionSaldo';

export default {
   components:{   
      AccionSaldo
   },
   data() {
      return {
         saldo: 1000,
         cuenta: "Visa",
         estado: true,
         servicios: ['Transferencias', 'Depósitos', 'Trarjetas de Crédito']
      }
   },
   methods: {
      aumentar(){
         this.saldo = this.saldo + 100;
      },

      disminuir(){
         this.saldo = this.saldo - 100;
      }
   }
}
</script>

<style>

</style>