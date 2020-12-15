<template>
	<a class="menu__submenu-text"  href="#">{{submenuText.innerText}}</a>
</template>

<script>
export default {
	name: "text",
	props: ["submenuText"]
}
</script>

<style scoped>
	.menu__submenu-text {
		display: block;
		border-top: 2px solid var(--menuGray);
		width: 100vw;
		margin: 0;
		padding: 0 0 0 10px;
		font-size: 12px;
		letter-spacing: 2px;
		line-height: 65px;
		color: var(--black);
		font-family: "Montserrat";
		cursor: pointer;
		-webkit-tap-highlight-color: transparent;
	}

	.menu__submenu-text:hover {
		color: var(--crimson);
	}
</style>