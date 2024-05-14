<script>
export default {
    data() {
        return {
            // imageName: "fotografia.webp"
        };
    },
    methods: {
        // getImagePath(img) {
        //     return new URL(`/src/assets/img/${img}`, import.meta.url).href;
        // }
    },
};
</script>

<template>
    <!-- hero -->
    <div class="bg-image">
        <div class="contacts">
            <h2>CONTACTS</h2>
            <div class="home-contacts">
                <router-link class="home" :to="{ name: 'home' }">Home</router-link>
                <span> / Contacts</span>
            </div>
        </div>
        <!-- <img :src="getImagePath(imageName)"> -->
    </div>
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