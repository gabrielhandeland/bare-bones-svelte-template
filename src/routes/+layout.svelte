<script lang="ts">
	import 'normalize.css';
	import Header from '$lib/Header.svelte';
</script>

<Header />
<div class="container">
	<slot />
</div>

<style lang="scss">
	:root {
		--background-color: #000000;
		--text-color: #ffffff;
	}

	:global(body) {
		background-color: var(--background-color);
		color: var(--text-color);
		margin: 0;
		height: 100vh;
		width: 100%;
		display: flex;
		flex-direction: column;
		font-family: 'Work Sans', sans-serif;
		font-size: 1rem;
	}

	:global(html) {
		min-width: 320px;
	}

	:global(a) {
		color: inherit;
		text-decoration: none;
	}

	:global(a:visited) {
		color: inherit;
	}

	.container {
		height: 100%;
		width: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	@media (max-width: 1000px) {
		:global(body) {
			font-size: 0.85rem;
		}
	}

	@media (max-width: 550px) {
		:global(body) {
			font-size: 0.75rem;
		}
	}
</style>
