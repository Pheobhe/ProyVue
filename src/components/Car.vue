<template lang="">
  <div>
    <h2>Coche </h2>
      <p>Marca: {{brand}}</p>
      <p>Modelo: {{model}}</p>
      <p>Color: {{color[2]}}</p>
      <p>Valor: {{precio}} U$S</p>
      <p>Potencia: {{power}} hp</p>
   <Test />
  </div>
</template>

<script>
import Test from "./Test";
export default{
  data() {
    return{
    brand:"Audi",
    model:"A4",
    color: "Negro",
    color: ["Azul", "Verde", "Negro"],
    precio: 38000,
    power:180,
  };
},
};


</script>
<style lang="">
  
</style>