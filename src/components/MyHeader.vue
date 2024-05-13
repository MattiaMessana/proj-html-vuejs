<script>
export default {
	data() {
		return {
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
};
</script>

<template>
	<header>
		<ul>
			<li v-for="item in menu">
				<router-link :to="{ name: item.routeName }" class="nav-link">
					{{ item.title }}
				</router-link>
			</li>
		</ul>
	</header>
</template>

<style scoped lang="scss">
header {
    height: 80px;
}
</style>
