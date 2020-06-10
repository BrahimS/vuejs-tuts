<template>
	<div id="app">
		<img alt="Vue logo" src="./assets/logo.png" />
		<HelloWorld :msg="message" para1="This is my first paragraph" />
		<div>
			<input type="text" v-model="message" />
			<button @click="handelClick" type="submit">Send</button>
		</div>
	</div>
</template>

<script>
	import HelloWorld from "./components/HelloWorld.vue";

	export default {
		name: "App",
		components: {
			HelloWorld,
		},
		data() {
			return {
				message: "This is my main message",
			};
		},
		methods: {
			handelClick() {
				console.log(`Your message: ${this.message}`);
			},
		},
	};
</script>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>
