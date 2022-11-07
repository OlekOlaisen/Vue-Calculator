<template>



	<section class="converter">

		<h1>Length converter</h1>


		<div class="converter-inputs">

			<label>mm</label>
			<input type="text" v-model="mm">
			<label>cm</label>
			<input type="text" v-model="cm">
			<label>m</label>
			<input type="text" v-model="m">
			<label>km</label>
			<input type="text" v-model="km">
		</div>

	</section>
</template>


<script>

export default {
	data() {
		return {
			mm: 0,
			cm: 0,
			m: 0,
			km: 0,
		}
	},

	watch: {

		km: function (val) {
			this.km = val;
			this.m = val * 1000;
			this.cm = val * 100000;
			this.mm = val * 1000000
		},

		m: function (val) {
			this.km = val / 1000;
			this.m = val;
		},

		cm: function (val) {
			this.km = val / 100000;
			this.m = val / 100;
			this.mm = val * 10;
			this.cm = val;
		},

		mm: function (val) {
			this.km = val / 1000000;
			this.m = val / 1000;
			this.cm = val / 10;
			this.mm = val;
		}

	},


}


</script>


<style scoped>
.converter {
	background-color: var(--background);
	border-radius: 1rem;
	width: 320px;
	height: 250px;
	margin-top: 1rem;
}

.converter-inputs {
	display: grid;
	grid-template-columns: repeat(2, 1fr);
	grid-template-rows: repeat(2, 1fr);
	gap: 1rem;
	justify-items: center;
	margin-top: 3rem;
	padding: 0 5rem;
}

p {
	color: white;
	margin: 0;
}

label {
	color: white;
	margin: 0 1rem;
}

input {
	width: 75px;
}
</style>