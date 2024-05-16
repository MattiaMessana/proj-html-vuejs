<template>
	<div class="text-start">
		<div class="overflow-hidden d-flex justify-content-center align-items-center">
			<img class="" :src="card.image" alt="" />
		</div>
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
img {
	width: 100%;
	transition: 0.5s;
	&:hover{
		transform: scale(1.05);
	}
}
p {
	font-size: 15px;
	letter-spacing: 0.6px;
}
h6 {
	text-transform: uppercase;
}
</style>
