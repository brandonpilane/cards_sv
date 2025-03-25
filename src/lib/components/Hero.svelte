<div class="hero__section">
	<div class="cards-container">
		<div class="cards"></div>
		<div class="cards"></div>
		<div class="cards"></div>
	</div>
	<div class="hero-copy">
		<h1>Cards</h1>
		<p>
			Learning <a href="https:\\svelte.dev" target="_blank">Svelte/Sveltekit</a> by building some cards
			UI.
		</p>
	</div>
</div>

<style>
	.hero__section {
		position: relative;
		padding-block: 5rem;
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.cards-container {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		gap: 2rem;
	}

	.cards {
		z-index: -1;
		height: 18rem;
		aspect-ratio: 13/17;
		border-bottom: none;
		border-radius: 2rem;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}

	.cards:nth-child(1) {
		transform: rotate(-10deg) translate(2rem, 5rem);
		background: linear-gradient(to bottom, #006400, transparent);
	}

	.cards:nth-child(2) {
		transform: rotate(-3deg) translate(0rem, 2rem);
		background: linear-gradient(to bottom, #38b000, transparent);
	}

	.cards:nth-child(3) {
		transform: rotate(10deg) translate(-3rem, 2rem);
		background: linear-gradient(to bottom, #9ef01a, transparent);
	}

	.hero-copy {
		position: absolute;
		bottom: 4rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 1rem;

		p,
		h1 {
			text-shadow: 0px 0px 5rem #fff;
		}

		a {
			text-decoration: dashed underline;
			font-weight: 100;
			transition: all 0.2s ease-in-out;

			&:hover {
				color: #006400;
			}
		}
	}

	a {
		color: black;
	}

	@media (prefers-color-scheme: dark) {
		.hero-copy p,
		.hero-copy h1 {
			text-shadow: 0px 0px 5rem #000;
		}

		a {
			color: white;

			&:hover {
				color: #9ef01a;
			}
		}
	}

	.hero-copy h1 {
		font-size: 5rem;
		font-weight: 900;
		text-align: center;
		text-transform: uppercase;
	}

	.hero-copy p {
		font-size: 1.5rem;
		text-align: center;
	}
</style>
