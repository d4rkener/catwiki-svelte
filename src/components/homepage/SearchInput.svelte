<div class="search hide-mobile">
	<input type="text" class="hide-mobile search__input" placeholder="Enter your breed" /><img
		class="search__logo"
		src="./search-outline.svg"
		alt="search-logo"
	/>
</div>

<style lang="scss">
	@use '../../scss/_variables.scss' as var;
	@use '../../scss/_breakpoints.scss' as md;

	.search {
		margin-top: 2.1875rem;

		@include md.breakpoint(large) {
			margin-top: 3rem;
		}

		&__input {
			padding: 1rem 2.625rem 1rem 1.5rem;
			border-radius: 3.6875rem;
			width: 15.625rem;
		}

		&__logo {
			width: 1.25rem;
			position: relative;
			right: 2.1875rem;
			top: 0.3125rem;
		}
	}
</style>
