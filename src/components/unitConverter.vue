<template>

	

	<section class="converter">
		
		<h1>Length converter</h1>
		
			
		<div class="converter-inputs">

				<input type="text">
				<select name="units" id="units">
					<option value="mm">mm</option>
					<option value="cm">cm</option>
					<option value="m">m</option>
					<option value="km">km</option>
				</select>

				<input type="text">	
				<select name="unitsConverted" id="unitsConverted">
					<option value="mm">mm</option>
					<option value="cm">cm</option>
					<option value="m">m</option>
					<option value="km">km</option>
				</select>
			
		</div>
			
	</section>
</template>


<script>

export default {
    data() {
        return {
        }
    },
}


</script>


<style scoped>

	.converter {
		background-color: var(--background);
		border-radius: 1rem;
		width: 320px;
		height: 200px;
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
		color:white;
		margin: 0 1rem;
	}

	input {
		width: 50px;
	}

	select {
		width: 50px;
	}



	


</style>