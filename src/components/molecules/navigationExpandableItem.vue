<template>
  <li>
		<div id="features" class="menu__expandable-item">
				<navigationText v-bind:item="item" v-bind:key="item.id" v-for="item in menuText"/>
				<div class="menu__right-arrow-outline">
						<img src="icons/arrow_right_black.svg" class="menu__arrow" alt="Black arrow right">
				</div>
		</div>
		<submenu/>
	</li>
</template>

<script>
	import navigationText from "../atoms/navigationText.vue"
	export default {
		name: "expandableItem",
		components: {
			navigationText
		},
		data() {
			return {
				menuText: [
					{
						id: 1,
						innerText: "features"
					}
				]
			}
		}
	}
	
</script>

<style>
	.menu__expandable-item {
		position: relative;
		cursor: pointer;
		-webkit-tap-highlight-color: transparent;
	}
	.menu__right-arrow-outline {
		display: flex;
		justify-content: space-around;
		position: absolute;
		right: 10px;
		top: 10px;
		border: 2px solid var(--menuGray);
		width: 43px;
		height: 43px;
	}
	.menu__text {
		display: block;
		border-top: 2px solid var(--menuGray);
		padding: 0 0 0 10px;
		text-transform: uppercase;
		font-size: 12px;
		letter-spacing: 2px;
		line-height: 65px;
		color: #000000;
		font-family: "Montserrat";
		-webkit-tap-highlight-color: transparent;
	}

	.menu__text:hover {
		color: var(--crimson);
	}

	.menu__right-arrow-outline {
		display: flex;
		justify-content: space-around;
		position: absolute;
		right: 10px;
		top: 10px;
		border: 2px solid var(--menuGray);
		width: 43px;
		height: 43px;
	}
	
	.menu__submenu-arrow-outline {
		right: 30px;
	}
</style>
