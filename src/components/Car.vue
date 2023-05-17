<template lang="">
  <div>
    <h2>Coche </h2>
      <p>Marca: {{brand}}</p>
      <p>Modelo: {{model}}</p>
      <p>Colores: 
       <!-- <span v-for ="(color, index) in colores" :key="index">
       {{index}}: {{ color }} - </span>  -->
       <ul>
        <li v-for ="(color, index) in colores" :key="index">
          {{index}}: {{ color }}
        </li>
       </ul>
      </p>
      <p>Valor: {{precio}} U$S</p>
     <!-- <p>Potencia: {{power}} hp</p>-->
      <p>Potencias</p>
      <ul>
       <template v-for="(power, index) in powers" :key="index">
          <li v-if="power < 280"> Urbana:{{ power }}</li>
          <li v-else-if="power === 280">Hibrido{{power}}</li>
          <li v-else> Carrera:{{ power }}</li>
          
          <li v-if="power >599"> Super:{{ power }}</li>
      </template>
     </ul>
    <!-- <p>Potencias Urbanas mayor a 300 hp </p>
      <ul>
       <template v-for="(power, index) in powers" :key="index">
          <li  v-if="power > 299" > 
             {{ power }}
          </li>
      </template>
     </ul>-->
   {{mensaje.title}} - {{mensaje.text}}
  </div>
</template>

<script>
export default{

 setup() {

  const brand ="Audi";
  const model = "A4";
  const colores = ["Negro", "Rojo", "Gris"];
  const precio = 45000;
  const powers = [60,80,120,10,200,240,280,300,390,540,500, 600,700];
  const mensaje ={
    title: "Hola Chango",
    text: "Adios Chango",
  }
  return{
    brand,
    model,
    colores,
    precio,
    powers,
    mensaje,
  };
 },
// },
};


</script>
<style lang="">
  
</style>