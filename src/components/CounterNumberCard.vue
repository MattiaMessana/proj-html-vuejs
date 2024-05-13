<template>
	<div>
		<h2>{{ card.number }}</h2>
		<h5>{{ card.title }}</h5>
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