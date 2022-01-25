<div class="search hide-desktop">
	<button class="search__button">Search <img src="./search-outline.svg" alt="search-logo" /></button
	>
</div>

<style lang="scss">
	@use '../../scss/_variables.scss' as var;

	.search {
		&__button {
			display: flex;
			font-size: 0.9375rem;
			padding: 0.5625rem 0.8125rem;
			gap: 0.875rem;
			border-radius: 3.6875rem;
			background-color: var.$white;
			margin-top: 1.125rem;

			&:active {
				opacity: 0.9;
			}

			img {
				width: 1.125rem;
			}
		}
	}
</style>
