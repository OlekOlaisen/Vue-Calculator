<template>
   <div class="calculator">
      <h1>Calculator</h1>
      <p class="calculator__input">0</p>
      <div class="calculator__operators">
         <button class="operator">/</button>
         <button class="operator">x</button>
         <button class="operator">-</button>
         <button class="operator">+</button>
         <button class="operator">CE</button>
      </div>
      <div class="calculator__buttons">
         <button class="button">1</button>
         <button class="button">2</button>
         <button class="button">3</button>
         <button class="button">4</button>
         <button class="button">5</button>
         <button class="button">6</button>
         <button class="button">7</button>
         <button class="button">8</button>
         <button class="button">9</button>
         <button class="button">0</button>
         <button class="operator">=</button>
      </div>

   </div>
</template>

<script>

</script>

<style scoped>
* {
   margin: 0;
   padding: 0;
   box-sizing: border-box;
}

h1 {
   font-weight: 500;
   font-family: Arial, Helvetica, sans-serif;
   font-size: 1rem;
   margin-left: 1rem;
   margin-top: 1rem;
}

.calculator {
   width: 320px;
   height: 530px;
   border: 1px solid black;
   margin: 2rem auto;
   border-radius: 1rem;
}

.calculator__input {
   width: 90%;
   height: 7rem;
   margin: 1rem auto;
   border-radius: 1rem;
   border: 1px solid black;
   font-size: 2rem;
   font-family: Arial, Helvetica, sans-serif;
}

.calculator__buttons {
   display: grid;
   grid-template-columns: repeat(3, 1fr);
   margin: 1rem;
   gap: 0.5rem;
   grid-column-end: span 1;
}

.calculator__operators {
   display: flex;
   gap: 0.5rem;
   justify-content: center;
   margin: 3rem 1rem 1rem;
}

.operator {
   border-radius: 0.3rem;
   border: none;
   padding: 1rem;
   width: 100%;
   background-color: grey;
   color: white;
}

.operator:hover {
   background-color: rgb(80, 80, 80);
}


.button {
   border-radius: 0.3rem;
   border: none;
   padding: 1rem;
   background-color: grey;
   color: white;
}

.button:nth-child(10) {
   background-color: lightgreen;
   grid-column: 1 / span 2;
}

.button:hover {
   background-color: rgb(80, 80, 80);
}
</style>