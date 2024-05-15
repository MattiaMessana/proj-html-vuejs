<script>
    export default {
        props: {
            pages: Object,
        }
    }
</script>

<template>

    <div class="bg-image">
        <div class="contacts">
            <h2>{{ pages.title }}</h2>
            <div class="home-contacts">
                <router-link class="home" :to="{ name: 'home' }">Home</router-link>
                <span> / {{ pages.span }}</span>
            </div>
        </div>
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