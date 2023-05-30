<template lang="">
    <div>
        <h1> Vue JS Props </h1>
     
        <CarProps :power="power" :brand="brand" :model="model" :upPower="upPower" />
       <p>Aca se pasaron variables mediante los props</p>
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
;
    return{
        brand,
        model,
        power,
        upPower,
    };
   },

};
</script>
<style lang="">
    
</style>