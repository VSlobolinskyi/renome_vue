<template>
	<li>
		<a class="cart-menu__text">{{item.innerText}}</a>
	</li>	
</template>

<script>

export default {
	name: 'cartMenuItem',
	props: ["item"]
}
</script>

<style scoped>
.cart-menu__text {
	display: block;
	margin: 0;
	padding: 15px 0;
	font-size: 12px;
	text-align: center;
	letter-spacing: 1px;
	color: var(--darkBlue);
	font-family: "Montserrat";
	-webkit-tap-highlight-color: transparent;
}

.cart-menu__text:hover {
	color: var(--crimson);
}
</style>
