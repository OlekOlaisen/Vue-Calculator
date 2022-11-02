<template>
   <div class="container">

      <div class="calculator">
         <h1>Calculator</h1>
         <div class="calculator-output">
            <p class="calculator-output__numbers">0</p>
         </div>

         <div class="calculator-buttons">
            <button class="button span-3 operator">CE</button>
            <button class="button operator">&divide;</button>
            <button class="button">7</button>
            <button class="button">8</button>
            <button class="button">9</button>
            <button class="button operator">x</button>
            <button class="button">4</button>
            <button class="button">5</button>
            <button class="button">6</button>
            <button class="button operator">-</button>
            <button class="button">1</button>
            <button class="button">2</button>
            <button class="button">3</button>
            <button class="button operator">+</button>
            <button class="button span-3">0</button>
            <button class="button operator">=</button>
         </div>

      </div>

   </div>
</template>

<script>

</script>

<style>
:root {

   --background: #344050;
   --background-operators: #404D5E;
   --background-output__numbers: #425062;
}


h1 {
   font-size: 1rem;
   color: white;
   margin: 0.5rem;
   font-family: Arial, Helvetica, sans-serif;
   text-align: center;

}

.calculator {
   max-width: 320px;
   background: var(--background);
   width: 320px;
   height: 530px;
   border: 1px solid black;
   margin: 1rem auto;
   border-radius: 1rem;
}

.calculator-output {
   font-family: Arial, Helvetica, sans-serif;
   font-size: 3rem;
   padding: 0.3rem;
   text-align: right;
   height: 100px;
   margin: 1rem;
   color: white;
}

.calculator-buttons {
   output: grid;
   grid-template-columns: repeat(4, 1fr);
   border: 0;
   gap: 0.2rem;
   margin: 2rem 1rem;

}

.span-2 {
   grid-column: span 2;
}

.span-3 {
   grid-column: span 3;
}

.button {
   font-size: 1rem;
   height: 65px;
   border: none;
   color: #fff;
   background-color: var(--background-output__numbers);
   border-radius: 0.3rem;
}

.button:hover {
   background: #627896;
}


.button:nth-child(1) {
   color: red;
   font-size: 1.2rem;
}

.button:nth-child(1):hover {
   background-color: rgb(240, 92, 92);
   font-size: 1.2rem;
   color: white;
}

.button:nth-child(16) {
   color: lightgreen;
   font-size: 1.2rem;
}

.button:nth-child(16):hover {
   background-color: lightgreen;
   font-size: 1.2rem;
   color: white;
}


.operator {
   background-color: #404D5E;
   color: #A8ADB5;
   font-size: 1.5rem;
}
</style>