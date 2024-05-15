<template>
	<div class="text-start">
		<img class="w-100" :src="card.image" alt="" />
		<p class="text-muted mt-3">{{ card.data }}</p>
		<h6 class="fw-bold fs-8">{{ card.title }}</h6>
		<p class="text-muted">{{ card.text }}</p>
	</div>
</template>

<script>
export default {
	props: {
		card: Object,
	},
};
</script>

<style lang="scss" scoped>
p {
	font-size: 15px;
	letter-spacing: 0.6px;
}
h6 {
	text-transform: uppercase;
}
</style>
