<template>
	<main>
		<Jumbotron />
		<section class="my-6">
			<div class="container text-center">
				<p class="fw-bold fs-7">PELICULA STUDIO</p>
				<h2 class="fw-bold">THIS IS WHAT WE DO</h2>
				<div class="cards row">
					<WhatWeDoCard class="col-4 mt-4" v-for="card in whatWeDoCards" :card="card" />
				</div>
			</div>
		</section>
		<AboutSection />
		<section class="my-6 best-hits">
			<div class="container text-center">
				<p class="fw-bold fs-7">YOUR WATCHLIST</p>
				<h2 class="fw-bold mb-4">BEST HITS MOVIES</h2>
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
		<section class="my-6 container text-center card-list-member">
			<CardListMember />
		</section>
		<PresentationSection />
		<section class="latest-news">
			<div class="container my-6 text-center">
				<div class="row">
					<p class="fw-bold fs-7">LATEST NEWS</p>
					<h2 class="fw-bold mb-4">ARTICLES UPDATED DAILY</h2>
					<LatestNewsCard class="col-4" v-for="card in latestNews" :card="card" />
				</div>
			</div>
		</section>
		<WidgetsSection />
		<section class="cta">
			<div class="container my-6">
				<div class="row">
					<div class="col-6">
						<p class="heading-class">COLLABORATE</p>
						<h3 class="title-cta">WANT TO WORK WITH US? LEAVE US A MESSAGE!</h3>
						<p class="text-muted text-justified">
							Duis sit amet congue ipsum. Nulla maximus My venenatis posuere.To The Mauris ut tempus
							Suspendisse porta tincidunt lectus non of me pellentesque. At A Sed blandit at diam sit
							amet Orci varius natoque penatibus et dis dis to parturient montes, My Car nascetur
							ridiculus Sed feugiat lacus in erat egestas, quis eleifend lacus imperdiet.
						</p>
					</div>
					<div class="col-6">
						<div class="row">
							<div class="col-6 mb-4">
								<input type="text" placeholder="Your Name" />
							</div>
							<div class="col-6 mb-4">
								<input type="text" placeholder="Your e-mail" />
							</div>
							<div class="col-6 mb-4">
								<input type="text" placeholder="Mobile number" />
							</div>
							<div class="col-6 mb-4">
								<input type="text" placeholder="Your Pincode" />
							</div>
							<div class="col-12 mb-4">
								<textarea rows="10" placeholder="Enter Your Message"></textarea>
							</div>
							<div class="col-12">
								<Button :text="'SUBMIT NOW'" />
							</div>
						</div>
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
import Button from "../components/Button.vue";
import AboutSection from "../components/AboutSection.vue";
import Jumbotron from "../components/Jumbotron.vue";
import WidgetsSection from "../components/WidgetsSection.vue";
import PresentationSection from "../components/PresentationSection.vue";

export default {
	components: {
		Jumbotron,
		WhatWeDoCard,
		BestHitsCard,
		CounterNumberCard,
		LatestNewsCard,
		CardListMember,
		Button,
		AboutSection,
		WidgetsSection,
		PresentationSection,
	},
	data() {
		return {
			whatWeDoCards: [
				{
					icon: "camera",
					title: "ARRAY OF EQUIPMENT",
					description: "Lorem ipsum dolor amet, consectetur ad",
				},
				{
					icon: "chair",
					title: "NEW TECHNOLOGIES",
					description:
						"Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
				},
				{
					icon: "sunglass",
					title: "VERSITILE ACTORS",
					description:
						"Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus",
				},
				{
					icon: "video",
					title: "TOP DIRECTORS",
					description:
						"Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus",
				},
				{
					icon: "cabaret",
					title: "MINUTE EDITING",
					description:
						"Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus",
				},
				{
					icon: "film",
					title: "VERSITILE ACTORS",
					description:
						"Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus",
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
			bestHits: [
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Gallery-01.jpg",
					title: "SEVENTEENTH SUMMER",
					type: "Commercial, Music Video.",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Gallery-02.jpg",
					title: "A MESSAGE TO SPACE",
					type: "Short Film",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Gallery-03.jpg",
					title: "THE MOST BEAUTIFUL THING",
					type: "Music Video",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Gallery-04.jpg",
					title: "PERMISSION TO SPEAK",
					type: "Documentary",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Gallery-05.jpg",
					title: "EXPLORE OUR SPACE",
					type: "Film noir",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Gallery-06.jpg",
					title: "FILM PRODUCTION",
					type: "Blaxploitation",
				},
			],
			latestNews: [
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/blog07.jpg",
					data: "November 06 , 2021 By Admin",
					title: "Recap your latest company event",
					text: "Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/blog01.jpg",
					data: "May 27 , 2022 By Admin",
					title: "How To Edit A Film Score To Serve ",
					text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Corporis est optio repellendus hic nisi. Quae.",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/blog02.jpg",
					data: "May 07 , 2022 By Admin",
					title: "Are You Ready To Make It Awesome",
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
@use "../style/variables" as *;

.counter-number {
	background-image: url(https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Parallax-01.jpg);
	color: white;
	/* Create the parallax scrolling effect */
	background-attachment: fixed;
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
}
.best-hits {
	h6 {
		font-weight: bold;
		font-size: small;
	}
	h2 {
		font-weight: bold;
	}
}
.presentation {
	min-height: 604px;
	background-image: url(../assets/img/bg-02.jpg);
	/* Create the parallax scrolling effect */
	background-attachment: fixed;
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
	color: white;
}
.widget-container {
	background-image: url(https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Parallax-03.jpg);
	/* Create the parallax scrolling effect */
	background-attachment: fixed;
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
}
.cta {
	input,
	textarea {
		width: 100%;
		background-color: $lightgray;
		border: 0;
		padding: 0.54em 1.3em;

		&:focus {
			outline: 0;
			box-shadow: 0px 5px 15px -7px rgba(0, 0, 0, 0.1);
		}
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
}
</style>
