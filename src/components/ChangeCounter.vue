<template>
	<button @click="addTwo">increment</button>
	<button @click="addEleven({ value: 10 })">increase</button>
</template>

<script>
import { mapActions } from 'vuex';
export default {
	methods: {
		// addOne() {
		// 	this.$store.dispatch('increment');
		// },
		// ...mapActions(['increment', 'increase']),
		...mapActions('numbers', {
			addTwo: 'increment',
			addEleven: 'increase',
		}),
	},
};
</script>