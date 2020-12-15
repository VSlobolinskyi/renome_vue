<template>
  <ul class="item-claster item-claster--submenu item-claster--hidden" id="featuresSubmenu">
		<li  v-bind:item="item" v-bind:key="item.id" v-for="item in submenuText" class="menu__submenu-item">
				<navsubmenuText/>
		</li>
	</ul>
</template>

<script>
	import navsubmenuText from "../atoms/navsubmenuText.vue"
	export default {
		name: "navigationSubmenu",
		components: {
			subnavigationText
		},
		data(){
			return {
				submenuText: [
					{
						id: 1,
						innerText: "One page"
					},
					{
						id: 2,
						innerText: "Portfolio"
					},
					{
						id: 3,
						innerText: "Shortcodes"
					}
				]
			}
		}
	}
</script>

<style scoped>
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

	.item-claster--submenu {
		position: absolute;
		top: 64px;
	}
</style>
