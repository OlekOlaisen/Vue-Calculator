<template>
   <section class="converter">
      <p>Celcius:</p>
      <input class="converter__input" type="number" placeholder="C" v-model="valueCelcius" />
      <p>Fahrenheit:</p>
      <div class="converter__output">{{ valueFahrenheit }} F</div>
   </section>
</template>


<script>

export default {
   data() {
      return {
         valueCelcius: 50,
      }
   },

   computed: {
      valueFahrenheit() {
         return (this.valueCelcius * 1.8) + 32;
      }
   }
}

</script>

<style scoped>
.converter {
   display: flex;
   flex-flow: column;

}

.converter__input {
   border: 1px solid white;
   margin: 1rem auto;
   width: 100px;
   height: 40px;
   font-size: 1rem;
   text-align: center;

}

.converter__output {
   color: white;
   border: 1px solid white;
   margin: 1rem auto;
   width: 100px;
   height: 40px;
   text-align: center;
   font-size: 1rem;
}

p {
   color: white;

}
</style>