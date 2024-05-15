<template>
	<div>
		<div class="mb-3 my-translate">
			<img :src="getPathImg()" alt="" />
		</div>
		<h5 class="mb-2">{{ card.title }}</h5>
		<p class="text-muted">{{ card.description }}</p>
	</div>
</template>

<script>
export default {
	props: {
		card: Object,
	},
	methods: {
		getPathImg() {
			return new URL(`../assets/img/${this.card.icon}.svg`, import.meta.url).href;
		},
	},
};
</script>

<style lang="scss" scoped>
img {
	width: 80px;
	height: 80px;
}
h5 {
	font-weight: 700;
	font-size: 17px;
	line-height: 1.4;
	letter-spacing: 0.6px;
}
.my-translate {
	transition: all 0.5s; /* Animation */

	&:hover {
		transform: translateY(-12px);
	}
}
</style>
