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
    }
</script>

<template>
    <div class="card  border-0 col-3" v-for="member in membersList">
        <img :src="member.image" class="card-img-top rounded" alt="">
        <div class="card-body">
            <h5 class="card-title"> {{ member.name }}</h5>
            <p class="card-text"> {{ member.role }}</p>
        </div>
</div>
</template>

<style scoped lang="scss">
   .card {
        img {
            max-width: 100%;
        }
   }
</style>