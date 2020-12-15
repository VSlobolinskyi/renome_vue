<template>
	<li class="menu__search-item">
			<input type="text" placeholder="Search..." maxlength="20" class="search__input" id="search">
			<img src="icons/search_icon.svg" class="search__icon search__icon--visible" id="searchIcon" alt="Search icon">
	</li>
</template>

<script>
export default {
	name: "search"
}
</script>

<style scoped>
	.menu_search-item {
		position: relative;
		display: flex;
	}

	.search__input {
		border: none;
		display: inline-block;
		padding-left: 10px;
		width: 100%;
		font-size: 12px;
		line-height: 65px;
		font-family: "Montserrat";
	}

	.search__input:focus {
		outline: none;
	}

	.search__input::placeholder {
		color: var(--inputGray);
		letter-spacing: 2px;
	}

	.search__icon {
		display: inline-block;
		position: absolute;
		right: 10px;
		width: 18px;
		height: auto;
		top: 18px;
	}

	.search__icon--hidden {
		display: none;
	}
</style>