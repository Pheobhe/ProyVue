<template lang="">
   
    <h2>Coche  - Composition API</h2>
      <p>Marca:    {{ brand }}</p>
      <p>Modelo:   {{ model }}</p>
      <p>Potencia: {{ power }} </p>
   <!-- <button @click="testPower">Aumentar</button> -->
    <button @click="upPower">Aumentar</button>
  </template>
  
  <script>

  export default{
    props:{
        brand:{
            type:String,
            default: "Audi",
        },
        model:{
            type:String,
            default: "A4",
        },
        power:{
            type:Number,
            default: 60,
        },

        upPower: Function,
    },

  setup(props) {
    
//     console.log(props);
//     const testPower =() =>{
//         props.upPower();
//     }
//    return{
//     testPower,
//    }
    }
  }
 

  </script> 
     
    <style lang="">
      
    </style>
 