<template>
	<p class="header__logo">Renome</p>
</template>

<script>
	
	export default {
		name: "headerLogo"
	}
</script>

<style lang="scss" scoped>
	@import "../../scss/_colors.scss";
	
	.header__logo {
		font-size: 25px;
		letter-spacing: 3px;
		padding: 0 0 0 10px;
		margin: 0;
		color: $black;
		font-family: "Pacifico";
		cursor: default;
	}
</style>
