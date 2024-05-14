<template>
	<button>
		{{ text }}
	</button>
</template>

<script>
export default {
	props: {
		text: String,
	},
};
</script>

<style lang="scss" scoped>
button {
	width: 100%;
	color: white;
	border: 0;
	background-color: black;
	padding: 12px 40px;
	font-weight: 700;
	font-size: 15px;
	line-height: 24px;
}
</style>
