<script>
export default {
	data() {
		return {
            logoTitle: "Cinematico-logo",
            imgLogo: "logo.svg",
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
	<header class="d-flex flex-row justify-content-between  p-3">
		
        <div>
			<router-link class="home" :to="{ name: 'home' }">
				<img :src="getImagePath(imgLogo)" :alt="logoTitle" class="align-self-center">
			</router-link>

        </div>

		<ul class="d-flex">
			<li v-for="item in menu" class="mx-2 align-self-center">
				<router-link :to="{ name: item.routeName }" class="nav-link zoom">
					{{ item.title }}
				</router-link>
			</li>
		</ul>
        <div>
            <ul class="d-flex">
                <li class="mx-2 zoom"><i class="fa-brands fa-facebook-f"></i></li>
                <li class="mx-2 zoom"><i class="fa-brands fa-youtube"></i></li>
                <li class="mx-2 zoom"><i class="fa-brands fa-instagram"></i></li>
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
		
        img {
            width: 150px;
        }
    }
	.zoom {
	padding: 5px;
	transition: transform .2s; /* Animation */
	}
	.zoom:hover {
	transform: scale(1.3);
	}
</style>
