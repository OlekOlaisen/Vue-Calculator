<template>
	<button @click="increaseCount">
		Current count: {{count}}
	</button>
</template>

<script>
	export default {
		data() {
			return {
				count: 0
			}
		},
		
		methods: {
			increaseCount() {
				this.count += 1;
			}
		}
	}
</script>

<style scoped>
	button {
		font-size: 2em;
		background: rgba(255, 0, 0, 0.1);
		border: 2px solid red;
		padding: 0.5em 2em;
		border-radius: 0.2em;
	}
</style>