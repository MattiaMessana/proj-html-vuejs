<template>
	<main>
		<section class="jumbotron">
			<div class="container h-100 d-flex align-items-center">
				<div>
					<p class="">CINEMA STUDIO</p>
					<h1 class="">DANCING WITH OF THE STARS</h1>
					<button>READ MORE</button>
				</div>
			</div>
		</section>
		<section class="my-6">
			<div class="container text-center">
				<h6>PELICULA STUDIO</h6>
				<h1>THIS IS WHAT WE DO</h1>
				<div class="cards row">
					<WhatWeDoCard class="col-4" v-for="card in whatWeDoCards" :card="card" />
				</div>
			</div>
		</section>
		<section class="about-us">
			<div class="container"></div>
		</section>
		<section class="my-6">
			<div class="container text-center">
				<h6>YOUR WATCHLIST</h6>
				<h1>BEST HITS MOVIES</h1>
				<div class="cards row">
					<BestHitsCard class="col-4" v-for="card in bestHits" :card="card" />
				</div>
			</div>
		</section>
		<section class="counter-number text-center py-6">
			<div class="container">
				<div class="row">
					<CounterNumberCard class="col-3" v-for="card in counterNumbers" :card="card" />
				</div>
			</div>
		</section>
	</main>
</template>

<script>
import WhatWeDoCard from "../components/WhatWeDoCard.vue";
import BestHitsCard from "../components/BestHitsCard.vue";
import CounterNumberCard from "../components/CounterNumberCard.vue";

export default {
	components: {
		WhatWeDoCard,
		BestHitsCard,
		CounterNumberCard,
	},
	data() {
		return {
			whatWeDoCards: [
				{
					icon: "icon",
					title: "title",
					description: "description",
				},
				{
					icon: "icon",
					title: "title",
					description: "description",
				},
				{
					icon: "icon",
					title: "title",
					description: "description",
				},
				{
					icon: "icon",
					title: "title",
					description: "description",
				},
				{
					icon: "icon",
					title: "title",
					description: "description",
				},
				{
					icon: "icon",
					title: "title",
					description: "description",
				},
			],
			bestHits: [
				{
					image: "image",
					title: "title",
					type: "type",
				},
				{
					image: "image",
					title: "title",
					type: "type",
				},
				{
					image: "image",
					title: "title",
					type: "type",
				},
				{
					image: "image",
					title: "title",
					type: "type",
				},
				{
					image: "image",
					title: "title",
					type: "type",
				},
				{
					image: "image",
					title: "title",
					type: "type",
				},
			],
			counterNumbers: [
				{
					number: "780",
					title: "SATISFIED CLIENTS",
				},
				{
					number: "20+",
					title: "OUR PROJECTS",
				},
				{
					number: "10,000",
					title: "CUP OF COFFEE",
				},
				{
					number: "12",
					title: "OUR AWARDS",
				},
			]
		};
	},
};
</script>

<style lang="scss" scoped>
.jumbotron {
	height: calc(100vh - 80px);
	background-color: lightcoral;
}
.about-us {
	min-height: 574px;
	background-color: black;
}
.counter-number {
	background-color: #000;
	color: white;
}
</style>
