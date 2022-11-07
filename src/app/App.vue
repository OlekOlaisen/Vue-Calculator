<template>
	<section class="website-container">

		<Calculator />
		<unitConverter />

	</section>

</template>

<script>


import Calculator from '../components/Calculator.vue';
import unitConverter from '../components/unitConverter.vue'

export default {
	components: {
		Calculator,
		unitConverter
	}
}
</script>

<style>
:root {

	--background: #344050;
	--background-operators: #404D5E;
	--background-output__numbers: #425062;
}

* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

.website-container {
	display: flex;
	flex-flow: row;
	align-items: center;
	justify-content: center;
	height: 100vh;
	background-color: rgb(240, 187, 137);
}

h1 {
	font-size: 1rem;
	color: white;
	margin: 0.5rem;
	font-family: Arial, Helvetica, sans-serif;
	text-align: center;

}
</style>