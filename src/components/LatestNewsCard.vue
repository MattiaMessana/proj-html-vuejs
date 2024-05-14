<template>
	<div>
		<p>{{ card.image }}</p>
		<p>{{ card.data }}</p>
		<h4>{{ card.title }}</h4>
		<p>{{ card.text }}</p>
	</div>
</template>

<script>
	export default {
		props: {
			card: Object,
		}
	}
</script>

<style lang="scss" scoped>

</style>