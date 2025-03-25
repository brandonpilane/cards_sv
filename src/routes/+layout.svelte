<script lang="ts">
	let { children } = $props();
</script>

<nav>
	<a href="/">Home</a>
	<a href="/about">About</a>
	<a href="/cards">Cards</a>
</nav>

{@render children()}

<style>
	nav {
		margin-top: 1rem;
		display: flex;
		position: relative;
		justify-content: center;
		width: 100%;
		gap: 5em;
		align-items: center;
	}

	a {
		padding: 1em;
		text-decoration: none;
		color: black;
		transition: all 0.2s ease-in-out;
		width: 6em;
		text-align: center;
		border-radius: 0.25em;
		font-weight: 800;
	}

	a:hover {
		color: white;
		background-color: black;
	}

	@media (prefers-color-scheme: dark) {
		a {
			color: white;
		}

		a:hover {
			background-color: white;
			color: black;
		}
	}
</style>
