<template>
	<a class="menu__submenu-text"  href="#">{{menuText.innerText}}</a>
</template>

<script>
export default {
	name: "navigationText",
	props: ["menuText"]
}
</script>

<style scoped>

</style>