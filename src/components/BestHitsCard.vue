<template>
	<div class="card text-center border border-0">
		<div class="overflow-hidden d-flex justify-content-center align-items-center">
			<img :src="card.image" class="zoom" alt="" />
		</div>
		<h5 class="card-title my-3">{{ card.title }}</h5>
		<p class="card-subtitle text-body-secondary mb-3">{{ card.type }}</p>
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
.card-title {
	font-weight: bold;
	font-size: medium;
}
.zoom {
	width: 100%;
	transition: transform 0.5s; /* Animation */
}
.zoom:hover {
	transform: scale(1.05);
}
</style>
