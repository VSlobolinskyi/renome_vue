<template>
	<div class="icons">
		<img v-on:click="$emit('toggle-cart-menu')" src='../../assets/icons/cart_icon.svg' class="icons__cart" >
		<p class="icons__cart-status">{{innerText}}</p>
		<div class="icons__stick"></div>
		<img v-on:click="$emit('open-menu')" src='../../assets/icons/hamburger_button.svg' class="icons__hamburger-button" id="bars">
		<img v-on:ckick="$emit('close-menu')" src='../../assets/icons/cross_icon.svg' class="icons__cross icons--hidden" id="cross">
	</div>
</template>

<script>
	export default {
		name: "headerIcons",
		data (){
			return {
				innerText: "5"
			}
		}
	}
</script>

<style lang="scss" scoped>
	@import "../../scss/_colors.scss";
	
	.icons {
		position: relative;
		display: flex;
		align-items: center;
		padding: 5px 10px 0 0;

		&__cart {
			display: inline-block;
			position: relative;
			padding: 0 3px;
			width: 15px;
			height: 12px;
			cursor: pointer;
			-webkit-tap-highlight-color: transparent;
		}

		&__cart-status {
		display: inline-block;
		position: relative;
		padding: 0 3px;
		font-size: 12px;
		letter-spacing: 2px;
		font-family: "Montserrat";
		cursor: default;
		}

		&__stick {
		display: inline;
		background-color: $black;
		margin: 0 3px;
		width: 1px;
		height: 15px;
		}

		&__hamburger-button {
		display: inline-block;
		position: relative;
		padding: 0 0 0 3px;
		width: 18px;
		height: 15px;
		cursor: pointer;
		-webkit-tap-highlight-color: transparent;
		}

		&__cross {
			display: inline-block;
			position: relative;
			height: 18px;
			padding: 0 0 0 3px;
			cursor: pointer;
			-webkit-tap-highlight-color: transparent;
		}
	}

	.icons--hidden {
		display: none
	}
</style>
