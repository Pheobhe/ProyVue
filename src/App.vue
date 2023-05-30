<template lang="">
    <div>
        <h1> Vue JS Props </h1>
     
        <CarProps :brand="brand"/>
       <p>Aca se pasaron variables mediante los props</p>
    </div>
  
</template>
<script>
import CarProps from "./components/CarProps"

export default {
    components: {
         CarProps,
    },
   
   setup(){
    
    let brand = "Audi";
    let model = "A4";
    let power = 30;
    return{
        brand,
        model,
        power,
    };
   },

};
</script>
<style lang="">
    
</style>