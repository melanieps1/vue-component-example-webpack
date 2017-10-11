<template>

	<div class="light">
		<bulb light-color="red" v-on:bulbClicked="catchBulbClick" />
		<bulb light-color="yellow" v-on:bulbClicked="catchBulbClick" />
		<bulb light-color="green" v-on:bulbClicked="catchBulbClick" />
	</div>

</template>

<script>

	import bulb from './bulb.vue';

	export default {
		name: 'light',
		components: {
			bulb
		},
		methods: {
			catchBulbClick: function(color) {
				this.$emit('lightClicked', color);
			}
		}
	}

</script>

<style>
	
	.light {
		background-color: #999;
		border: 2px solid #000;
		display: block;
		margin: auto;
		width: 66px;
	}

</style>