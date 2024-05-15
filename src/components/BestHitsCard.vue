<template>
	<div class="card text-center border border-0">
        <img :src="card.image" class="card-img-top zoom" alt="">
		<div class="card-body">
			<h5 class="card-title">{{ card.title }}</h5>
			<p class="card-subtitle text-body-secondary">{{ card.type }}</p>
		</div>
	</div>
</template>

<script>
	export default {
		props: {
			card: Object
		}
	}
</script>

<style lang="scss" scoped>
.zoom {
  padding: 10px;
  transition: transform .2s; /* Animation */
}
.zoom:hover {
  transform: scale(1.1);
}
</style>