<template>
	<div>
		<h2>Quotes Added</h2>
		<div class="progress">
		  <div class="progress-bar" role="progressbar" aria-valuenow="70" aria-valuemin="0" aria-valuemax="100" :style="{ width: (quotesCount * 10) + '%'}">
		    <div v-if="quotesCount > 0">{{ quotesCount}} / 10</div> 
		  </div>
		</div>
	</div>
</template>

<script>
	export default {
		props: ['quotesCount']
	}
</script>

<style scoped>
</style>