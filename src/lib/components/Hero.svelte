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

	<div class="bg_pattern">
		<div class="shape"></div>
		<div class="shape"></div>
		<div class="shape"></div>
		<div class="shape"></div>
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

	.bg_pattern {
		z-index: -4;
		position: absolute;
		width: 100vw;
		height: 100vh;
		top: 0;

		.shape {
			z-index: inherits;
			position: absolute;
			width: 200px;
			height: 200px;
			background-color: #9ef01aa4;
			filter: blur(80px);
			border-radius: 50%;
			animation: float 20s infinite alternate ease-in-out;
		}

		/* Position different shapes randomly */
		.shape:nth-child(1) {
			width: 400px;
			height: 200px;
			top: 10%;
			left: 20%;
			animation-duration: 25s;
			animation-direction: alternate-reverse;
		}

		.shape:nth-child(2) {
			background-color: #38b0008f;
			width: 300px;
			height: 300px;
			bottom: 10%;
			left: 27%;
			animation-duration: 30s;
			animation-delay: 10s;
		}

		.shape:nth-child(3) {
			background-color: #33c733a4;
			top: 56%;
			left: 66%;
			animation-duration: 35s;
			animation-delay: 3s;
			animation-direction: alternate-reverse;
		}

		.shape:nth-child(4) {
			top: 22%;
			left: 80%;
			animation-duration: 40s;
		}
	}

	/* .bg_pattern::before {
			content: '';
			position: absolute;
			width: 100vw;
			height: 80vh;
			top: 0;
			left: 0;
			z-index: 10;
			border-radius: 3rem;

			box-shadow:
				/* inset 0 0 1rem #101010,
				inset 0 0 1rem #101010,
				inset 0 0 1rem #101010,
				inset 0 0 1rem #101010,
				inset 0 0 1rem #101010,
				inset 0 0 1rem #101010,
				inset 0 0 1rem #101010,
				inset 0 0 1rem #101010, 
				inset 0 0 1rem #101010,
				inset 0 0 1rem #101010;
		} */

	/* Animation for smooth floating */
	@keyframes float {
		0% {
			transform: translate(0, 0) scale(1); /* Start at the origin */
		}
		25% {
			transform: translate(10rem, -16rem) scale(1.1); /* Move to the right and up */
		}
		50% {
			transform: translate(30rem, -3em) scale(1); /* Move to the far right */
		}
		75% {
			transform: translate(9.2rem, 12rem) scale(0.9); /* Move down and right */
		}
		100% {
			transform: translate(2rem, 17rem) scale(1); /* Return to the origin */
		}
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
		bottom: -3rem;
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
		padding-block: 0;
		padding: 0;
		font-size: 10rem;
		text-align: center;
		text-transform: uppercase;
		letter-spacing: 0.25em;
	}

	.hero-copy p {
		font-size: 1.5rem;
		text-align: center;
	}
</style>
