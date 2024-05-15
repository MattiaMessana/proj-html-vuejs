<script>
    export default {
        data() {
            return {
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

<style lang="scss" scoped>
  .widget-container {
        background-image: url(https://wordpressthemes.live/WP02/WP031/wp-content/uploads/2022/08/Parallax-03.jpg);
        background-position: center;
        background-size: cover;
    }

</style>