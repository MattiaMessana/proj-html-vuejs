<script>
export default {
	data() {
		return {
            logoTitle: "Cinematico-logo",
            imgLogo: "otherLogo.jpg",
			menu: [
				{
					title: "Home",
					routeName: "home",
				},
				{
					title: "About",
					routeName: "about",
				},
				{
					title: "Contacts",
					routeName: "contacts",
				},
			],

		};
	},
    methods: {
            getImagePath(imageName) {
                return new URL(`../assets/img/${imageName}`, import.meta.url).href;
            },
        },
};
</script>

<template>
	<header class="d-flex flex-row justify-content-around text-center align-items-center p-3">
        <div>
            <img :src="getImagePath(imgLogo)" :alt="logoTitle">
        </div>
		<ul class="d-flex">
			<li v-for="item in menu" class="mx-2">
				<router-link :to="{ name: item.routeName }" class="nav-link">
					{{ item.title }}
				</router-link>
			</li>
		</ul>
        <div>
            <ul class="d-flex">
                <li class="mx-2"><i class="fa-brands fa-facebook-f"></i></li>
                <li class="mx-2"><i class="fa-brands fa-youtube"></i></li>
                <li class="mx-2"><i class="fa-brands fa-instagram"></i></li>
            </ul>
        </div>
	</header>
</template>

<style scoped lang="scss">
    header {
		position: fixed;
    	top: 0;
    	left: 0;
    	width: 100%;
    	z-index: 9999;
		background-color: white;
		// debug
        height: 80px;
        img {
            width: 70px;
        }
    }
</style>
