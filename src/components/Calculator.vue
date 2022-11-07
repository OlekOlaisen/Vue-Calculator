<template>

   <div class="calculator">
      <h1>Calculator</h1>

      <div class="calculator-output">
         {{ showingResult ? currentResult : currentInput }}

      </div>

      <div class="calculator-input">
         <button @click="clearResult" class="button span-3 operator">C</button>
         <button @click="handleOperatorInput('/')" class="button operator">/</button>
         <button @click="handleNumberInput(7)" class="button">7</button>
         <button @click="handleNumberInput(8)" class="button">8</button>
         <button @click="handleNumberInput(9)" class="button">9</button>
         <button @click="handleOperatorInput('*')" class="button operator">*</button>
         <button @click="handleNumberInput(4)" class="button">4</button>
         <button @click="handleNumberInput(5)" class="button">5</button>
         <button @click="handleNumberInput(6)" class="button">6</button>
         <button @click="handleOperatorInput('-')" class="button operator">-</button>
         <button @click="handleNumberInput(1)" class="button">1</button>
         <button @click="handleNumberInput(2)" class="button">2</button>
         <button @click="handleNumberInput(3)" class="button">3</button>
         <button @click="handleOperatorInput('+')" class="button operator">+</button>
         <button @click="handleNumberInput(0)" class="button span-3">0</button>
         <button @click="handleEqualsInput" class="button operator">=</button>
      </div>

   </div>
</template>

<script>

export default {
   data() {
      return {
         currentResult: 0,
         currentInput: 0,
         currentOperator: null,
         showingResult: false,
      }
   },

   created() {
      addEventListener('keyup', this.handleKeyup);
   },

   computed: {
      currentInputAsNumber() {
         return Number(this.currentInput)
      },
   },



   methods: {
      calculateResult() {
         switch (this.currentOperator) {
            case '+':
               this.currentResult += this.currentInputAsNumber;
               break;
            case '-':
               this.currentResult -= this.currentInputAsNumber;
               break;
            case '/':
               this.currentResult /= this.currentInputAsNumber;
               break;
            case '*':
               this.currentResult *= this.currentInputAsNumber;
               break;
            default:
               this.currentResult = this.currentInputAsNumber;
         }
      },

      clearResult() {
         this.currentResult = 0;
         this.currentInput = 0;
         this.currentOperator = null;
         this.showingResult = false;
      },

      handleOperatorInput(operator) {
         this.calculateResult();
         this.currentOperator = operator;
         this.currentInput = '';
         this.showingResult = true;
      },

      handleNumberInput(digit) {
         this.currentInput += digit;
         this.showingResult = false;
      },

      handleEqualsInput() {
         this.calculateResult();
         this.showingResult = true;
      },

   }
}

</script>

<style scoped>
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
   margin-top: 1rem;
   margin-right: 3rem;
   border-radius: 1rem;
   border: none;
   box-shadow: 3px 3px 10px rgb(32, 32, 32);
}

.calculator-output {
   font-family: Arial, Helvetica, sans-serif;
   font-size: 3rem;
   padding: 0.3rem;
   text-align: right;
   height: 100px;
   margin: 1rem;
   color: white;
   position: relative;
}

small {
   font-size: 1rem;
   position: absolute;
   bottom: 0;
   left: 50%;
   color: grey;
}

.calculator-input {
   display: grid;
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
   color: #f05c5c;
   font-size: 1.2rem;
}

.button:nth-child(1):hover {
   background-color: #f05c5c;
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
   color: black;
}

.operator {
   background-color: #404D5E;
   color: #A8ADB5;
   font-size: 1.5rem;
}
</style>