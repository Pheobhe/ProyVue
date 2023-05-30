<template lang="">
   
    <h2>Coche  - Composition API</h2>
      <p>Marca:    {{ brand }}</p>
      <p>Modelo:   {{ model }}</p>
      <p>Potencia: {{ power }} </p>
    
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
    },

  setup(props) {
    //const brand ="Audi";
    //const model = "A4";
  //console.log(props);
//   return{
//       brand,
//       model,
    
//     };
  },
  };
  </script>
  
    <style lang="">
      
    </style>