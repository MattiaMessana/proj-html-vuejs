<script>
export default {
	props: {
		cardObj: Object,
	},
	data() {
		return {
			membersList: [
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Team-01.jpg",
					name: "Fabricio Guerra",
					role: "Main Director",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Team-02.jpg",
					name: "Umberto Pagoda",
					role: "Main Writer",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Team-03.jpg",
					name: "Gloria Riccasso",
					role: "Main Producer",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Team-04.jpg",
					name: "Lio Napoin",
					role: "Cameraman",
				},
			],
		};
	},
};
</script>

<template>
	<div class="row text-center">
		<p class="fw-bold fs-7">THE PERICUROS</p>
		<h2 class="mb-5 fw-bold">MEET THE TEAM</h2>
		<div class="card border-0 col-3" v-for="member in membersList">
			<img :src="member.image" class="card-img-top rounded zoom" alt="" />
			<div class="card-body">
				<h5 class="card-title">{{ member.name }}</h5>
				<p class="card-text">{{ member.role }}</p>
			</div>
		</div>
	</div>
</template>

<style scoped lang="scss">
.card {
	img {
		max-width: 100%;
	}
}
.zoom {
	width: 100%;
	transition: transform 0.5s; /* Animation */
}
.zoom:hover {
	transform: scale(1.05);
}
</style>
