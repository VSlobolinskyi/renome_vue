<template>
	<div class="header">
		<headerLogo/>
		<headerIcons  v-on:toggle-cart-menu="toggleCartMenu"  v-on:open-menu="toggleCartMenu"  v-on:close-menu="toggleCartMenu"/>
		<cartMenu/>
		<navigationMenu/>
	</div>
</template>

<script>
	import headerLogo from "../atoms/headerLogo.vue"
	import cartMenu from "../molecules/cartMenu.vue"
	import headerIcons from "../molecules/headerIcons"
	import navigationMenu from "../molecules/navigationMenu.vue"
	export default {
		name: 'face',
		components: {
			cartMenu,
			headerLogo,
			headerIcons,
			navigationMenu
		},
		methods: {
			toggleCartMenu() {
				let cartMenuReference = document.getElementById("cartMenu")
				cartMenuReference.classList.remove("cart-menu--hidden");
				cartMenuReference.classList.toggle("cart-menu--fade");
					function cartMenuHide() {
						if (!cartMenuReference.classList.contains("cart-menu--fade")) {
							cartMenuReference.classList.add("cart-menu--hidden");
						}
						clearTimeout(cartTimout);
					}
				let cartTimout = setTimeout(cartMenuHide, 400);
			},
			openMenu() {
				let cross = document.getElementById("corss");
				let bars = document.getElementById("bars");
				cross.classList.toggle("icons--hidden");
				bars.classList.toggle("icons--hidden");
				body.classList.add("body--disable-scroll");
				menu.classList.add("item-claster--visible");
				menu.classList.remove("menu--hidden");
				menu.classList.toggle("menu--fade");
			},
			closeMenu() {
				let cross = document.getElementById("corss");
				let bars = document.getElementById("bars");
				let menu = document.getElementById("root");
				let body = document.getElementById("body");
				cross.classList.toggle("icons--hidden");
				bars.classList.toggle("icons--hidden");
				menu.classList.toggle("menu--fade");
				body.classList.remove("body--disable-scroll");
				function resetMenu() {
					let back = document.getElementById("back");
					let clasterToHide = document.getElementById(submenuOrder[submenuOrder.length - 1]);
					clasterToHide.classList.add("item-claster--hidden");
					clasterToHide.classList.remove("item-claster--visible");
					submenuOrder.forEach( submenuId => {
						if(submenuId != "root") { 
							document.getElementById(submenuId).classList.add("item-claster--submenu");
						}
					});
					menu.classList.remove("item-claster--hidden");
					menu.classList.remove("item-claster--visible");
					back.classList.add("back--hidden");
					back.classList.remove("back--visibles");
					menu.classList.add("menu--hidden");
					submenuOrder = ["root"];
					clearTimeout(navigationTimout);
				}
				let navigationTimout = setTimeout(resetMenu, 400);
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
