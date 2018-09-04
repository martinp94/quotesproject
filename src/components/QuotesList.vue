<template>
	<div class="row">
		<app-quote v-for="quote in quotes">
			<h1 slot="text">{{ quote }}</h1> 
		</app-quote>
	</div>
</template>

<script>
	import Quote from './Quote.vue';

	export default {
		props: ['quotes'],
		components: {
			appQuote: Quote
		}
	}
</script>

<style scoped>
</style>