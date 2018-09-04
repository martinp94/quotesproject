<template>
    <div class="container">
    	<div class="row">
    		<div class="col-xs-12">
    			<app-header :quotesCounter="quotesCounter"></app-header>
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
        		quotesCounter: 0
        	}
        },
        components: {
        	appHeader: Header,
        	appAddQuotes: AddQuotes,
        	appQuotesList: QuotesList,
        	appFooter: Footer
        }
    }
</script>

<style>
</style>
