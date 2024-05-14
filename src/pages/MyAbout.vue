<script>
import BestHitsCard from '../components/BestHitsCard.vue';
import CardListMember from '../components/CardListMember.vue';

    export default {
        components: {
            BestHitsCard,
            CardListMember,
        },
        data() {
            return {
                
			bestHits: [
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Gallery-01.jpg",
					title: "Seventeenth Summer",
					type: "Commercial, Music Video.",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Gallery-02.jpg",
					title: "A Message to Space",
					type: "Short Film",
				},
				{
					image: "https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Gallery-03.jpg",
					title: "The most beautiful thing",
					type: "Music Video",
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
    }
</script>

<template>

    <div class="bg-image">
        <div class="contacts">
            <h2>ABOUT</h2>
                <div class="home-contacts">
                    <router-link class="home" :to="{ name: 'home' }">Home</router-link>
                    <span> / About</span>
                </div>
        </div>
    </div>

       
    <div class="cards row px-5 text-center mb-5 mt-3">
        <h5 class="mt-4">YOUR WATCHLIST</h5>
        <h2 class="mb-5">BEST HITS MOVIES</h2>
        <BestHitsCard class="col-4" v-for="card in bestHits" :card="card" />
    </div>

    
    <div class="MySection d-flex align-items-center">
        <div class="container"></div>
        <div class="container p-4">
            <span>ABOUT US</span>
            <h3 class="my-3">HIGH QUALITY CINEMATIC</h3>
            <p>
                Orci varius penatibus et magnis dis parturient In the montes, nascetur ridiculus mus. Nulla
                A nisi ut mi efficitur hendrerit. nunc urna. quisque a partr hendrerit purus erat, nec dapibus
                sem sed. phasellus sed eli molestie, porttitor ligula of the egestas, mattis augue. quisque et
                rhoncus justo. suspendisse luctus pharetra eleme tcondimentum.
            </p>
            <button class="btn btn-light rounded-0 px-4">READ MORE</button>
        </div>
        
    </div>

    <section class="my-6 container text-center">
		<CardListMember />
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
       
</template>

<style scoped lang="scss">
    .bg-image {
    background-image: url(/src/assets/img/bredcum-img.jpg);
    background-size: cover;
    background-position: center;

    .contacts {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        padding: 100px;

        h2 {
            color: white;
            font-size: 3rem;
        }

        .home-contacts {
            color: white;

            .home {
                color: white;
            }
        }
    }
}
    .MySection {
        color: white;
        background-color: black;
        // debug
        min-height: 500px;
    }
    
    .widget-container {
	    background-color: black;
    }


</style>