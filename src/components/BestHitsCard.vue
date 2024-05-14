<template>
	<div class="card text-center border border-0">
		<p>{{ card.image }}</p>
		<div class="card-body">
			<h5 class="card-title">{{ card.title }}</h5>
			<p class="card-subtitle text-body-secondary">{{ card.type }}</p>
		</div>
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