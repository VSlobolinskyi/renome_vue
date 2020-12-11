<template>
	<div class="header">
		<cartMenu/>
	</div>
</template>

<script>
	import cartMenu from "../molecules/cartMenu.vue"
	export default {
		name: 'face',
		components: {
			cartMenu
		},
		methods: {
			toggleCartMenu() {
				cartMenu.classList.remove("cart-menu--hidden");
				cartMenu.classList.toggle("cart-menu--fade");
					function cartMenuUndisplay() {
						if (!cartMenu.classList.contains("cart-menu--fade")) {
						cartMenu.classList.add("cart-menu--hidden");
						}
						clearTimeout(cartTimout);
					}
				let cartTimout = setTimeout(cartMenuUndisplay, 400);
			}
		}
	}
</script>

<style scoped>
	.header {
		position: fixed;
		display: flex;
		justify-content: space-between;
		width: 100%;
		height: 45px;	
		top: 0;
		padding: 0 0 10px;
		background-color: var(--white);
		z-index: 2;
	}
</style>
