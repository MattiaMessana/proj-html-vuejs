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
		<section class="my-6 container text-center">
			<CardListMember />
		</section>
		<section class="presentation">
			<div class="container py-6 text-center w-50">
				<i class="fa-solid fa-quote-left quotation-marks"></i>
				<p>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore optio fugiat vitae, quisquam
					itaque vel explicabo numquam! Laborum, illo! Rerum sint velit quo excepturi est perspiciatis a
					ex eveniet voluptatibus?
				</p>
			</div>
		</section>
		<section class="latest-news">
			<div class="container my-6 text-center">
				<div class="row">
					<h6>LATEST NEWS</h6>
					<h1>ARTICLES UPDATED DAILY</h1>
					<LatestNewsCard class="col-4" v-for="card in latestNews" :card="card" />
				</div>
			</div>
		</section>
		<section class="widget-container py-7">
			<div class="container">
				<div class="row">
					<div v-for="widget in widgets" class="col-3 d-flex justify-content-center">
						<img class="w-75" :src="getPathImg(widget)" alt="" />
					</div>
				</div>
			</div>
		</section>
		<section class="cta">
			<div class="container my-6">
				<div class="row">
					<div class="col-6">
						<p class="text-cta">COLLABORATE</p>
						<h3 class="title-cta">WANT TO WORK WITH US? LEAVE US A MESSAGE!</h3>
					</div>
				</div>
			</div>
		</section>
	</main>
</template>

<script>
import WhatWeDoCard from "../components/WhatWeDoCard.vue";
import BestHitsCard from "../components/BestHitsCard.vue";
import CounterNumberCard from "../components/CounterNumberCard.vue";
import LatestNewsCard from "../components/LatestNewsCard.vue";
import CardListMember from "../components/CardListMember.vue";

export default {
	components: {
		WhatWeDoCard,
		BestHitsCard,
		CounterNumberCard,
		LatestNewsCard,
		CardListMember,
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
			],
			Team: [
				{
					image: "image",
					name: "name",
					work: "work",
				},
				{
					image: "image",
					name: "name",
					work: "work",
				},
				{
					image: "image",
					name: "name",
					work: "work",
				},
				{
					image: "image",
					name: "name",
					work: "work",
				},
			],
			latestNews: [
				{
					image: "image",
					data: "data",
					title: "title",
					text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Corporis est optio repellendus hic nisi. Quae.",
				},
				{
					image: "image",
					data: "data",
					title: "title",
					text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Corporis est optio repellendus hic nisi. Quae.",
				},
				{
					image: "image",
					data: "data",
					title: "title",
					text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Corporis est optio repellendus hic nisi. Quae.",
				},
			],
			widgets: ["01", "02", "03", "04"],
		};
	},
	methods: {
		getPathImg(fileName) {
			return new URL(`../assets/img/${fileName}.png`, import.meta.url).href;
		},
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
.presentation {
	min-height: 604px;
	background-color: black;
	color: white;

	.quotation-marks {
		padding-top: 30px;
		font-size: 70px;
	}
}
.widget-container {
	background-color: rgba($color: #000000, $alpha: 0.8);
}
.text-cta {
	font-weight: bold;
	font-size: small;
}
.title-cta {
	font-size: 40px;
	line-height: 50px;
	font-weight: bold;
}
</style>
