<template>
	<div>
		<p>{{ card.image }}</p>
		<h5>{{ card.title }}</h5>
		<p>{{ card.type }}</p>
	</div>
</template>

<script>
	export default {
		props: {
			card: Object
		}
	}
</script>

<style lang="scss" scoped>

</style>