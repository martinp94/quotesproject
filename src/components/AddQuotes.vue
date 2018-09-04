<template>
	<div>

		<div class="row">
			<div class="col-xs-12 col-xs-offset-4">
				<h3>Quote</h3>
			</div>
		</div>

		<div class="row">
			<div class="col-xs-12 col-xs-offset-4">
				<textarea ref="quote" v-model="quote" class="input" cols="62" rows="5"></textarea>
			</div>
		</div>

		<div class="row">
			<div class="col-xs-2 col-xs-offset-6">
				<button @click="addQuote" class="btn btn-primary">Add Quote</button>
			</div>
		</div>
		
	</div>
</template>

<script>
	export default {
		data() {
			return {
				quote: ''
			}
		}, 
		methods: {
			addQuote() {

				if(this.quote) {
					this.$emit('newQuote', this.quote);
					this.quote = ''; 
				}
			}
		},
        updated() {
        	this.$refs.quote.focus();
        }
	}
</script>

<style scoped>
	textarea {
		resize: none;
	}
</style>