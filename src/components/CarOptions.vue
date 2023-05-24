<template lang="">
   
      <h2>Coche  - Options API</h2>
        <p>Marca: {{brand}}</p>
        <p>Modelo: {{model}}</p>
        <p>Potencia: {{power}}</p>
        <button @click="upPower(50)"> Aumentar</button>
        <button @click="downPower"> Disminuir</button>
  
  </template>
  
  <script>
  export default{
    data() {
      return{
      brand: "Seat",
      model: "Leo",
      power: 60,
      };
    } ,
    methods: {
      upPower(newPower) {
        console.log("Aumentar Potencia");
        console.log(this.power);
        //this.power = this.power +1;
       // this.power++;
        this.power = this.power + newPower;
      },
      downPower(){
        console.log("Disminuir Potencia");
        this.power--;
      }
    },
  };
  </script>
 