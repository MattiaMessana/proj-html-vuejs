<template>
	<div>
		<p>{{ card.icon }}</p>
		<h5>{{ card.title }}</h5>
		<p>{{ card.description }}</p>
	</div>
</template>

<script>
	export default {
		props:{
			card: Object,
		}
	}
</script>

<style lang="scss" scoped>

</style>