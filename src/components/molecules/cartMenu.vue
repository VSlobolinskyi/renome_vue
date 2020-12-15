<template>
	<ul class="cart-menu" id="cartMenu">
		<cartMenuItem v-bind:item="item" v-bind:key="item.id"  v-for="item in cartMenuItems" />
	</ul>
</template>

<script>
	import cartMenuItem from '../atoms/cartMenuItem.vue'

	export default {
		name: 'cartMenu',
		data(){
			return {
				cartMenuItems: [
					{
						id: 1,
						innerText: "$44.50"
					},
					{
						id: 2,
						innerText: "View cart"
					},
					{
						id: 3,
						innerText: "Checkout"
					}
				]
			}
		},
		components: {
			cartMenuItem
		}
	}

</script>

<style lang="scss" scoped>
	.cart-menu {
		position: fixed;
		list-style-type: none;
		opacity: 0;
		top: 44px;
		background-color: var(--white);
		padding: 0;
		margin: 0;
		width: 115px;
		height: 138px;
		right: 35px;
		z-index: 3;
		transition: opacity 0.4s, top 0.4s;
	}

	.cart-menu--fade {
		opacity: 1;
		top: 54px;
	}

	.cart-menu--hidden {
		pointer-events: none;
	}
</style>
