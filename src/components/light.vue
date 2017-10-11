<template>

	<div class="light">
		<bulb light-color="red" v-on:red="catchRed()" />
		<bulb light-color="yellow" v-on:yellow="catchYellow()" />
		<bulb light-color="green" v-on:green="catchGreen()" />
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
			catchRed: function() {
				alert('red light clicked');
			},
			catchYellow: function() {
				alert('yellow light clicked');
			},
			catchGreen: function() {
				alert('green light clicked');
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