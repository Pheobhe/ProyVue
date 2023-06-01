cars props
<template lang="">
   
    <h2>Coche  - Composition API</h2>
      <p>Marca:    {{ brand }}</p>
      <p>Modelo:   {{ model }}</p>
      <p>Potencia: {{ power }} </p>
  
    <button @click="upPower">Aumentar</button>
   <!-- <button @click="downPower">Disminuir</button> -->
    <button @click="downPowerFn">Disminuir</button>
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
        downPower: Function,
    },

  emits: ["downPower"] ,

  setup(props, context) {
    console.log(context);

    const downPowerFn =() => {
      context.emit("downPower");
      console.log("hola");

    }
//     console.log(props);
//     const testPower =() =>{
//         props.upPower();
//     }
    return{
    downPowerFn,
   }   

    }
  }
 

  </script> 
     
   