<template>
    <div class="container">
    
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
