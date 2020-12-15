<template>
	<ul class="menu menu--hidden item-claster" id="root">
		<back/>
		<search/>
		<li v-bind:item="item" v-bind:key="item.id" v-for="item in menuText">
				<navigationText/>
		</li>
		<navigationExpandableItem/>
	</ul>
</template>

<script>
	import back from "./backItem.vue"
	import search from "./searchItem.vue"
	import navigationExpandableItem from "./navigationExpandableItem.vue"
	import navigationText from "../atoms/navigationText.vue"
	export default {
		name: "navigationMenu",
		components: {
			back,
			search,
			navigationExpandableItem,
			navigationText
		},
		data() {
			return {
				menuText: [
					{
						id: 1,
						innerText: "home"
					},
					{
						id: 2,
						innerText: "about"
					},
					{
						id: 3,
						innerText: "menu"
					},
					{
						id: 4,
						innerText: "reservations"
					},
					{
						id: 5,
						innerText: "blog"
					},
					{
						id: 6,
						innerText: "shop"
					},
					{
						id: 7,
						innerText: "contact"
					}
				]
			}
		}
	}
</script>

<style>
	.item-claster {
		background-color: var(--white);
		flex-direction: column;
		list-style-type: none;
		padding: 0;
	}

	.item-claster--hidden {
		height: 0;
		visibility: hidden;
		pointer-events: none;
		list-style-type: none;
		padding: 0;
	}

	.item-claster--visible {
		visibility: visible;
		pointer-events: initial;
		max-height: 70vh;
		overflow-y: scroll;
		overflow-x: hidden;
	}

	.menu {
		list-style-type: none;
		opacity: 0;
		top: 28px;
		position: fixed;
		width: 100%;
		padding: 0;
		background-color: var(--white);
		z-index: 2;
		transition: opacity 0.4s, top 0.4s;
	}

	.menu--fade {
		opacity: 1;
		top: 38px;
		width: 100%;
	}

	.menu--hidden {
		pointer-events: none;
		width: 100%;
	}
</style>
