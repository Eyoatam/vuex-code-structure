<template>
	<button @click="login" v-if="!isAuth">Login</button>
	<button @click="logout" v-if="isAuth">Logout</button>
	<p>{{ isAuth }}</p>
</template>

<script>
import { mapGetters } from 'vuex';
import { mapActions } from 'vuex';
export default {
	methods: {
		...mapActions(['login', 'logout']),
	},
	computed: {
		...mapGetters({
			isAuth: 'userIsAuth',
		}),
	},
};
</script>