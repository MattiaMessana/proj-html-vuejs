<script>
export default {
	data() {
		return {
			widgets: ["01", "02", "03", "04", "01", "02", "03", "04"],
		};
	},
	methods: {
		getPathImg(fileName) {
			return new URL(`../assets/img/${fileName}.png`, import.meta.url).href;
		},
	},
};
</script>

<template>
	<section class="widget-container py-7">
		<div class="container">
				<div class="d-flex justify-content-center">
					<Splide
						data-splide='{"pagination": false, "autoplay": true, "interval": 4000, "perPage": 5, "arrows": false, "perMove": 1 }'
						class="h-100 position-relative"
						:options="{ rewind: true }"
						aria-label="My Favorite Images"
					>
						<SplideSlide v-for="widget in widgets" class="col-3">
							<img :src="getPathImg(widget)" alt="" />
							<div class="my-overlay"></div>
						</SplideSlide>
						
						

					</Splide>
				</div>
			</div>
	</section>
</template>

<style lang="scss" scoped>
.widget-container {
	background-image: url(https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Parallax-03.jpg);
	background-position: center;
	background-size: cover;
	
	/* Create the parallax scrolling effect */
	background-attachment: fixed;
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
}
</style>
