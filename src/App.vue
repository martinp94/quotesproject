<template>
    <div class="container">
    	<app-header :quotesCount="quotes.length"></app-header>
    	<app-add-quotes @newQuote="newQuote"></app-add-quotes>

		<app-quotes-list :quotes="quotes"
						 @quoteDeleted="deleteQuote"></app-quotes-list>

		<br>

		<div class="row">
			<div class="col-sm-12 text-center">
				<div class="alert alert-info">
					Info: Click on a Quote to Delete it!
				</div>
			</div>
		</div>
    </div>
</template>

<script>
	
	import Header from './components/Header.vue';
	import AddQuotes from './components/AddQuotes.vue';
	import QuotesList from './components/QuotesList.vue';
	import Footer from './components/Footer.vue';

    export default {
        data() {
        	return {
        		quotesMax: 10,
        		quotes: []
        	}
        },
        components: {
        	appHeader: Header,
        	appAddQuotes: AddQuotes,
        	appQuotesList: QuotesList,
        	appFooter: Footer
        },
        methods: {
        	newQuote(quote) {
        		if(this.quotes.length < this.quotesMax)
        			this.quotes.push(quote);
        		else
        			alert('Please delete quotes first!');
        	},
        	deleteQuote(index) {
        		this.quotes.splice(index, 1);
        	}
        }
    }
</script>

<style>
</style>
