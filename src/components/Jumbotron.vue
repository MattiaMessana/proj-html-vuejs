<template>
	<section class="jumbotron">
		<Splide
			data-splide='{"pagination": false}'
			class="h-100 position-relative"
			:options="{ rewind: true }"
			aria-label="My Favorite Images"
		>
			<SplideSlide class="overflow-hidden">
				<img :src="getPathImg('01')" alt="Sample 1" />
				<div class="my-overlay"></div>
			</SplideSlide>
			<SplideSlide>
				<img :src="getPathImg('07')" alt="Sample 2" />
				<div class="my-overlay"></div>
			</SplideSlide>
		</Splide>
		<div class="my-container container position-absolute top-0 h-100 d-flex align-items-center">
			<div class="text-white">
				<p class="fw-bold fs-7">CINEMA STUDIO</p>
				<h1 class="fw-bold mb-4">DANCING WITH OF THE STARS</h1>
				<Button class="w-fit bg-white text-black" :text="'READ MORE'" />
			</div>
		</div>
	</section>
</template>

<script>
import Button from "./Button.vue";

export default {
	components: {
		Button,
	},
	methods: {
		getPathImg(fileName) {
			return new URL(`../assets/img/${fileName}.jpg`, import.meta.url).href;
		},
	},
};
</script>

<style lang="scss" scoped>
.jumbotron {
	height: calc(100vh - 80px);
	background-color: lightcoral;

	ul {
		height: calc(100vh - 80px);
	}
	li {
		display: flex;
		justify-content: center;
		align-items: center;
		overflow: hidden;
		height: calc(100vh - 80px);
	}
	ul.splide__pagination {
		display: none !important;
	}
	.my-container {
		left: 8%;
		width: 100vw;
	}
}
.my-overlay {
	width: 100%;
	height: 100%;
	background-color: rgba(0, 0, 0, 0.6);
	position: absolute;
	left: 0;
	top: 0;
}
img {
	width: 100%;
	min-height: 100%;
	object-fit: cover;
	object-position: center;
}
</style>
