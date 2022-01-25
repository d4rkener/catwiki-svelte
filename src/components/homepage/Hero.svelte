<script>
	import SearchInput from './SearchInput.svelte';
	import SearchButton from './SearchButton.svelte';
</script>

<div class="hero">
	<img src="./catwiki-logo-light.svg" alt="logo" class="hero__logo" />
	<p class="hero__paragraph">Get to know more about your <br /> cat breed</p>
	<SearchInput />
	<SearchButton />
</div>

<style lang="scss">
	@use '../../scss/_variables.scss' as var;
	@use '../../scss/_breakpoints.scss' as md;

	.hero {
		background-image: url('./hero-image-sm.png');
		background-repeat: no-repeat;
		background-position: center;
		background-size: cover;
		border-top-left-radius: 2.625rem;
		border-top-right-radius: 2.625rem;
		padding: 1.5625rem 1.875rem;
		color: var.$white;

		@include md.breakpoint(medium) {
			background-image: url('./hero-image-md.png');
			padding: 3.125rem 3.75rem;
		}

		@include md.breakpoint(large) {
			background-image: url('./hero-image-lg.png');
			padding: 4.6875rem 5.625rem;
		}

		&__logo {
			width: 6.25rem;

			@include md.breakpoint(medium) {
				width: 9.375rem;
			}

			@include md.breakpoint(large) {
				width: 15.625rem;
			}
		}

		&__paragraph {
			font-size: 0.875rem;

			@include md.breakpoint(medium) {
				font-size: 1.125rem;
			}

			@include md.breakpoint(large) {
				font-size: 1.5rem;
			}
		}
	}
</style>
