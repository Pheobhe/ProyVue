appvue
<template lang="">
  <div>
      <h1> Vue JS Props </h1>
   
      <CarProps :power="power" :brand="brand" :model="model" :upPower="upPower" @downPower="downPower"/>
     <p>Aca se pasaan las funciones mediante @ ej: @downPower="downPower", siempre es mas limpio el cod sin el @ Conslusion: es mas limpio usar props que emits</p>
  </div>

</template>
<script>
import {ref} from "vue";
import CarProps from "./components/CarProps"

export default {
  components: {
       CarProps,
  },
 
 setup(){
  
  let brand = "Audi";
  let model = "A3";
  let power = ref(38);

const upPower =() => {
  console.log("Aumentar power ...");
  power.value++;
}
const downPower =() => {
  console.log("Disminuir power ...");
  power.value--;
}
;
  return{
      brand,
      model,
      power,
      upPower,
      downPower,
  };
 },

};
</script>
<style lang="">
  
</style>