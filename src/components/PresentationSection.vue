<template>
	<section class="presentation">
		<div class="container py-6 text-center w-50">
			<i class="fa-solid fa-quote-left quotation-marks"></i>
			<Splide
				data-splide='{"autoplay": false, "perPage": 1, "arrows": false, "perMove": 1 }'
				class="h-100 position-relative"
				:options="{ rewind: true }"
				aria-label="My Favorite Images"
			>
				<SplideSlide v-for="presentation in presentations">
					<div class="pt-5 my-slide">
						<p>
							Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam vero magni ipsam
							sapiente consequuntur, nostrum atque obcaecati natus alias autem, aliquid tempora quo
							eius commodi ducimus temporibus dolorem. Architecto, dolor.
						</p>
						<div class="d-flex justify-content-center align-items-center">
							<img :src="presentation.img" alt="" />
							<div class="text-start px-2 d-flex flex-column justify-content-center">
								<h6 class="m-0">{{ presentation.name }}</h6>
								<p class="m-0">{{ presentation.role }}</p>
							</div>
						</div>
					</div>
				</SplideSlide>
			</Splide>
		</div>
	</section>
</template>

<script>
export default {
	data() {
		return {
			presentations: [
				{
					img: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/01.jpg",
					name: "JON DOE",
					role: "Desiner",
				},
				{
					img: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/02.jpg",
					name: "JON DOE",
					role: "Desiner",
				},
				{
					img: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/03.jpg",
					name: "JON DOE",
					role: "Desiner",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.quotation-marks {
	padding-top: 30px;
	font-size: 70px;
}
img {
	border-radius: 50%;
	width: 56px;
}
.my-slide {
	transform: translateY(-40px);
}
</style>
