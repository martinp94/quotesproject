<template>
	<div class="row">
		<app-quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">
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
		},
		methods: {
			deleteQuote(index) {
				this.$emit('quoteDeleted', index);
			}
		}
	}
</script>

<style scoped>
</style>