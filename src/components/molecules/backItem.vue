<template>
	<li class="menu__back-item back--hidden" id="back">
			<p class="back-item__text">back</p>
			<div class="menu__left-arrow-outline">
					<img src="icons/arrow_left_black.svg" class="menu__arrow" alt="Black arrow left">
			</div>
	</li>
</template>

<script>
	export default {
		name: "back"
	}
</script>

<style scoped>
	.menu__back-item {
		position: relative;
	}

	.back--hidden {
		display: none;
	}

	.back--visible {
		visibility: visible;
		pointer-events: auto;
		background-color: var(--white);
		cursor: pointer;
		-webkit-tap-highlight-color: transparent;
	}

	.back-item__text {
		text-align: right;
		text-transform: uppercase;
		margin: 0;
		padding: 0 10px 0 0;
		font-size: 12px;
		letter-spacing: 2px;
		line-height: 65px;
		color: var(--black);
		font-family: "Montserrat";
	}

	.back-item__text:hover {
		color: var(--crimson);
	}

	.menu__left-arrow-outline {
		display: flex;
		justify-content: space-around;
		position: absolute;
		left: 10px;
		top: 10px;
		border: 2px solid var(--menuGray);
		width: 43px;
		height: 43px;
	}
</style>
