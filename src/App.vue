<template lang="">
    <div>
        <h1> Vue JS </h1>
        <CarOptions />
        <hr />
        <CarComposition />
        <hr />
      <!--<Car /> -->
    </div>
   <p>"Lore" </p>
</template>
<script>
// import Car from "./components/Car"
import CarComposition from "./components/CarComposition"
import CarOptions from "./components/CarOptions"
export default {
    components: {
        CarComposition,
        CarOptions,
        // Car,
    }
}
</script>
<style lang="">
    
</style>