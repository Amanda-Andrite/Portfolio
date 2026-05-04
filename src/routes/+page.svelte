<script>
	import { resolve } from '$app/paths';
	import { contactInfoOpen } from '$lib/stores/contact.js';
</script>

<svelte:head>
	<title>Portfolio</title>
</svelte:head>

<main class="page">
	<section class="intro">
		<header class="intro-content">
			<h1>Meet the creative mind behind the screen.</h1>
			<p>
				I design and develop websites that balance aesthetics with functionality, bringing bold
				ideas to life through purposeful design and clean, efficient code.
			</p>
			<p>
				My websites dont just look good, they perform. From concept to launch, I craft experiences
				that are intuitive, responsive, and built to last.
			</p>
			<button on:click={() => contactInfoOpen.set(true)}> Contact Me </button>
		</header>
	</section>

	<div class="primary-divider"></div>
	<div class="secondary-divider"></div>

	<section class="about" aria-labelledby="about-title">
		<div class="about-container">
			<div class="about-image">
				<div class="image-placeholder"></div>
			</div>

			<article class="about-content">
				<h2 id="about-title" class="about-title">ABOUT ME</h2>
				<div class="about-card">
					<p class="about-text">Hello</p>
					<p class="about-email">@email.com</p>
				</div>
			</article>
		</div>
	</section>

	<div class="primary-divider"></div>
	<div class="secondary-divider"></div>

	<section class="links">
		<div class="links-container">
			<a href={resolve('/skills')} class="circle circle-1" aria-label="Go to My Skills page">
				<div class="circle-shape"></div>
				<span>My Skills</span>
			</a>
			<a href={resolve('/contact')} class="circle circle-2" aria-label="Go to Contact page">
				<div class="circle-shape"></div>
				<span>Contacts</span>
			</a>
			<a href={resolve('/work')} class="circle circle-3" aria-label="Go to My Work page">
				<div class="circle-shape"></div>
				<span>My Work</span>
			</a>
			<a href={resolve('/qs')} class="circle circle-4" aria-label="Go to Q/A page">
				<div class="circle-shape"></div>
				<span>Q/A</span>
			</a>
		</div>
	</section>
</main>

<style>
	.page {
		display: flex;
		flex-direction: column;
	}

	.intro {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding-left: 4rem;
		padding-right: 2rem;
		margin-bottom: 0;
		padding-bottom: 3rem;
	}

	.intro-content {
		max-width: 550px;
	}

	h1 {
		font-family: var(--font-heading);
		font-size: 2.5rem;
	}

	p {
		font-family: var(--font-body);
		font-size: 1.2rem;
	}

	button {
		margin-top: 1rem;
		padding: 0.8rem 1.8rem;
		font-family: var(--font-heading);
		background-color: var(--color-button);
		font-size: 1.1rem;
		cursor: pointer;
		color: white;
	}

	.primary-divider {
		height: 30px;
		background-color: var(--divider-color);
		margin: 0;
	}

	.secondary-divider {
		height: 50px;
		background-color: var(--background-tertiary);
		margin: 0;
	}

	.about {
		background-color: var(--background-secondary);
		padding: 2rem 1rem;
		display: flex;
		justify-content: center;
		margin: 0;
	}

	.about-container {
		display: flex;
		gap: var(--gap-lg);
		align-items: center;
		width: 100%;
		max-width: 1400px;
		padding: 0 4rem;
		flex-wrap: wrap;
	}

	.image-placeholder {
		width: 450px;
		height: 580px;
		aspect-ratio: 3 / 4;
		border-radius: var(--card-radius);
		background: var(--background-tertiary);
		display: flex;
		align-items: center;
		justify-content: center;
		position: relative;
		overflow: hidden;
	}

	.image-placeholder::after {
		content: 'IMAGE';
		color: var(--color-white);
		font-family: var(--font-heading);
		font-size: 2rem;
	}

	.about-content {
		display: flex;
		flex-direction: column;
		flex: 1;
		align-items: center;
		justify-content: center;
		gap: 0.5rem;
	}

	.about-title {
		background-color: var(--background-primary);
		color: var(--text-primary);
		font-family: var(--font-heading);
		padding: 0.6rem 1.5rem;
		border-radius: var(--radius-md);
		width: fit-content;
		font-size: 3rem;
		letter-spacing: 2px;
		margin: 0;
	}

	.about-card {
		width: 100%;
		max-width: 500px;
		height: 450px;
		min-height: 250px;
		background-color: var(--background-primary);
		padding: 0.8rem;
		border-radius: var(--card-radius);
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		margin: 0 auto;
	}

	.about-text {
		font-family: var(--font-body);
		color: var(--text-primary);
	}

	.about-email {
		font-size: var(--font-sm);
		text-align: center;
		color: var(--text-primary);
	}

	/*grid background*/
	.links {
		background-color: var(--background-primary);
		padding: 3rem 2rem 4rem;
		background-image:
			linear-gradient(to right, rgba(0, 0, 0, 0.05) 1px, transparent 1px),
			/*vertical lines*/ linear-gradient(to bottom, rgba(0, 0, 0, 0.05) 1px, transparent 1px); /*horizontal lines*/
		background-size: 40px 40px; /*grid size*/
	}

	.links-container {
		position: relative;
		width: 100%;
		max-width: 900px;
		height: 400px;
		margin: 0 auto;
	}

	.circle {
		position: absolute;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 0.5rem;
		cursor: pointer;
		text-decoration: none;
		color: inherit;
	}

	.circle-shape {
		width: 150px;
		height: 150px;
		border-radius: 50%;
		border: 3px solid #5a4634;
		background-color: transparent;
		transition: transform 0.2s ease;
	}

	.circle:hover .circle-shape {
		transform: scale(1.05); /*Responsive hover effect */
	}

	/* Position the circles */
	.circle span {
		font-family: var(--font-button);
		font-size: 1rem;
	}

	.circle-1 {
		left: 0;
		bottom: 40px;
	}
	.circle-2 {
		left: 25%;
		top: 0;
	}
	.circle-3 {
		right: 25%;
		top: 0;
	}
	.circle-4 {
		right: 0;
		bottom: 40px;
	}

	/* Accessibility, styles for keyboard nav */
	.circle:focus-visible .circle-shape {
		outline: 3px solid var(--color-button);
	}

	/* Responsive styles */
	@media (max-width: 768px) {
		/* intro section */
		.intro {
			flex-direction: column;
			align-items: flex-start;
			padding: 2rem 1.5rem;
			gap: 1.5rem;
		}

		.intro-content {
			max-width: 100%;
		}

		h1 {
			font-size: 2rem;
			line-height: 1.2;
		}

		p {
			font-size: 1rem;
		}

		button {
			width: 100%;
			max-width: 220px;
		}

		/* about section */
		.about-container {
			flex-direction: column;
			align-items: center;
			text-align: center;
			padding: 0 1.5rem;
			gap: 2rem;
		}

		.about-content {
			display: flex;
			flex-direction: column;
			align-items: center;
			width: 100%;
			order: 0;
			gap: 1rem;
		}

		.image-placeholder {
			max-width: 350px;
			width: 100%;
			height: 375px;
		}
		.about-card {
			order: 2;
			width: min(450px, 70vw);
			height: 375px;
			padding: 1rem;
		}

		.about-title {
			font-size: 1.8rem;
			padding: 0.4rem 1rem;
		}

		/* links section */
		.links-container {
			transform: scale(0.8);
			transform-origin: center;
			height: 400px;
		}

		.circle {
			gap: 0.4rem;
		}

		.circle-shape {
			width: 150px;
			height: 150px;
		}

		.circle span {
			font-size: 0.85rem;
		}

		.circle-1 {
			left: -70px;
			bottom: 25px;
		}

		.circle-2 {
			left: 8%;
			top: 10px;
		}

		.circle-3 {
			right: 8%;
			top: 10px;
		}

		.circle-4 {
			right: -70px;
			bottom: 25px;
		}
	}

	/* Further adjustments for very small screens */
	@media (max-width: 480px) {
		.links-container {
			transform: scale(0.8);
			transform-origin: center;
			height: 400px;
		}

		.circle {
			gap: 0.4rem;
		}

		.circle-shape {
			width: 140px;
			height: 140px;
		}

		.circle span {
			font-size: 0.85rem;
		}

		.circle-1 {
			left: -70px;
			bottom: 25px;
		}

		.circle-2 {
			left: 3%;
			top: 10px;
		}

		.circle-3 {
			right: 3%;
			top: 10px;
		}

		.circle-4 {
			right: -70px;
			bottom: 25px;
		}
	}
</style>
