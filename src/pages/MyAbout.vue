<script>
import AboutSection from '../components/AboutSection.vue';
import BestHitsCard from '../components/BestHitsCard.vue';
import CardListMember from '../components/CardListMember.vue';
import WidgetsSection from '../components/WidgetsSection.vue';


    export default {
        components: {
            BestHitsCard,
            CardListMember,
            AboutSection,
            WidgetsSection,
            
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
            };
        },
    }
</script>

<template>

    <!-- hero -->

        <div class="bg-image">
            <div class="contacts">
                <h2>ABOUT</h2>
                <div class="home-contacts">
                    <router-link class="home" :to="{ name: 'home' }">Home</router-link>
                    <span> / About</span>
                </div>
            </div>
        </div>

    <!-- /hero -->

    


    <!-- BestHitsCard  -->

        <div class="cards row px-5 text-center mb-5 mt-3">
            <h5 class="mt-4">YOUR WATCHLIST</h5>
            <h2 class="mb-5">BEST HITS MOVIES</h2>
            <BestHitsCard class="col-4" v-for="card in bestHits" :card="card" />
        </div>

    <!-- /BestHitsCard  -->



    <!-- AboutSection -->

        <AboutSection />

    <!-- /AboutSection -->


    
    <!-- CardListMember -->

        <section class="my-6 container text-center">
            <CardListMember />
        </section>

    <!-- /CardListMember -->


    <!-- WidgetsSection -->

        <WidgetsSection />

    <!-- WidgetsSection -->

       
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
    

</style>