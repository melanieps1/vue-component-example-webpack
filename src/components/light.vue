<template>

	<div class="light">
		<bulb light-color="red" />
		<bulb light-color="yellow" />
		<bulb light-color="green" />
	</div>

</template>

<script>

	import bulb from './bulb.vue';

	export default {
		name: 'light',
		components: {
			bulb
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