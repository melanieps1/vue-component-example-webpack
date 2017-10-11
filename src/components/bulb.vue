<template>
	
	<div class="bulb" v-bind:class="lightColor" v-on:click="reportClickToParent(lightColor)"></div>

</template>

<script>
	
	export default {
		name: 'bulb',
		props: ['lightColor'],
		methods: {
			reportClickToParent: function(colorClicked) {
				// We are emitting an event and passing `colorClicked`
				this.$emit('bulbClicked', colorClicked);
			}
		}
	}

</script>

<style>
	
	.bulb {
		background-color: #ccc;
		border: 2px solid #000;
		border-radius: 50%;
		height: 50px;
		margin: 5px;
		width: 50px;
	}

	.green {
		background-color: #0f0;
	}

	.yellow {
		background-color: #ff0;
	}

	.red {
		background-color: #f00;
	}

</style>