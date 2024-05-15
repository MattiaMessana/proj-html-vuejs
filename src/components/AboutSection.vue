<template>
	<section class="about-us text-white">
		<div class="container min-height">
			<div class="row min-height">
				<div class="col-6 min-height"></div>
				<div class="col-6 min-height d-flex flex-column justify-content-center">
					<span class="fw-bold fs-7">ABOUT US</span>
					<h2 class="mt-3">HIGH QUALITY CINEMATIC</h2>
					<p class="my-4">
						Orci varius penatibus et magnis dis parturient In the montes, nascetur ridiculus mus. Nulla
						A nisi ut mi efficitur hendrerit. nunc urna. quisque a partr hendrerit purus erat, nec
						dapibus sem sed. phasellus sed eli molestie, porttitor ligula of the egestas, mattis augue.
						quisque et rhoncus justo. suspendisse luctus pharetra eleme tcondimentum.
					</p>
					<Button class="bg-white text-black w-fit" :text="'READ MORE'"/>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
import Button from "./Button.vue";
export default {
	components: {
		Button,
	}
};
</script>

<style lang="scss" scoped>
.about-us {
	min-height: 574px;
	background-image: url(../assets/img/About-Us.jpg);
	span {
		letter-spacing: 2px;
	}
	h2 {
		font-size: 32px;
	}
}
.min-height {
	min-height: 574px;
}
</style>
