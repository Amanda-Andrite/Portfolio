<script>
	import { resolve } from '$app/paths';
	import { base } from '$app/paths';
	import { contactInfoOpen } from '$lib/stores/contact.js';
</script>

<svelte:head>
	<title>Portfolio</title>
</svelte:head>

<main class="page">
	<section class="intro">
		<div class="intro-board">
			<div class="intro-paper">
				<header class="intro-content">
					<h1>Meet the creative mind behind the screen.</h1>
					<p>
						I like turning ideas into visuals, whether that’s rough wireframes, concept art, or 3D.
						It’s all about figuring things out visually and shaping the direction early on.
					</p>
					<p>
						From simple sketches to more detailed 3D work, I use design to explore how things could
						look and work before they’re built, keeping everything clear and intentional.
					</p>
					<button class="contact-btn" on:click={() => contactInfoOpen.set(true)}>
						Contact Me
						<img class="whatsapp-icon" src="{base}/icons/whatsapp.png" alt="WhatsApp" />
					</button>
				</header>
			</div>
			<div class="sticky-notes">
				<div class="sticky-note note-1"><p>Design with purpose</p></div>
				<div class="sticky-note note-2"><p>Design with purpose</p></div>
				<div class="sticky-note note-3"><p>Design with purpose</p></div>
			</div>
		</div>
	</section>

	<div class="primary-divider"></div>
	<div class="secondary-divider"></div>

	<section class="about" aria-labelledby="about-title">
		<div class="about-container">
			<div class="about-image">
				<img class="profile-image" src="{base}/profile.jpg" alt="Profile" />
			</div>

			<article class="about-content">
				<h2 id="about-title" class="about-title">ABOUT ME</h2>
				<div class="about-card">
					<p class="about-text">
						I’m Amanda Andrite. I grew up always designing, planning, and organising anything I
						could get my hands on. I naturally leaned towards creating order and clarity.
					</p>
					<p class="about-text">
						I care a lot about design, especially creating things that don’t feel overwhelming or
						strained. I’m drawn to making work that feels calm, clear, and easy to move through.
						Over time, that turned into a real passion.
					</p>
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
				<div class="circle-shape"><img src="{base}/icons/skills.png" alt="Skills icon" /></div>
				<span>My Skills</span>
			</a>
			<button
				type="button"
				on:click={() => contactInfoOpen.set(true)}
				class="circle circle-2"
				aria-label="Open Contact modal"
			>
				<div class="circle-shape">
					<img src="{base}/icons/contact.png" alt="Contact icon" />
				</div>
				<span>Contacts</span>
			</button>

			<a href={resolve('/work')} class="circle circle-3" aria-label="Go to My Work page">
				<div class="circle-shape"><img src="{base}/icons/work.png" alt="Work icon" /></div>
				<span>My Work</span>
			</a>
			<a href={resolve('/qs')} class="circle circle-4" aria-label="Go to Q/A page">
				<div class="circle-shape"><img src="{base}/icons/qa.png" alt="QA icon" /></div>
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

	.intro-board {
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		gap: 1rem;
		flex-wrap: wrap;
		position: relative;
	}

	.intro-paper {
		background: white;
		padding: 1rem;
		max-width: 530px;
		border-radius: 8px;
		transform: translateY(-10px) rotate(-1deg);
		box-shadow: 4px 6px 0 rgba(0, 0, 0, 0.15);
	}

	.intro {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem 2rem;
		background-image:
			linear-gradient(rgba(0, 0, 0, 0.12) 2px, transparent 2px),
			linear-gradient(90deg, rgba(0, 0, 0, 0.12) 2px, transparent 2px);
		background-size: 50px 50px;
		border: 2px solid var(--background-tertiary);
		border-radius: 12px;
		max-width: 1300px;
		margin: 2rem auto;
		position: relative;
		overflow: hidden;
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

	.contact-btn {
		margin-top: 1rem;
		padding: 0.8rem 1.8rem;
		font-family: var(--font-heading);
		background-color: var(--color-button);
		border-radius: 15px;
		font-size: 1.1rem;
		cursor: pointer;
		color: white;
		display: inline-flex;
		align-items: center;
		gap: 0.6rem;
	}

	.whatsapp-icon {
		width: 40px;
		height: 40px;
		object-fit: contain;
	}

	.sticky-notes {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		z-index: 5;
		margin-top: 2rem;
		margin-left: 1.5rem;
	}

	.sticky-note {
		width: 160px;
		min-height: 120px;
		background: #fbffbe;
		padding: 1rem;
		box-shadow: 4px 6px 0 rgba(0, 0, 0, 0.15);
		font-family: var(--font-body);
		font-size: 10px;
		color: var(--text-primary);
		display: flex;
		align-items: center;
		justify-content: center;
		text-align: center;
		transform: rotate(-2deg);
	}

	.note-1 {
		transform: rotate(-4deg);
	}

	.note-2 {
		transform: rotate(2deg);
		margin-left: 20px;
	}

	.note-3 {
		transform: rotate(-1deg);
		margin-left: -10px;
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

	.profile-image {
		width: 450px;
		height: 580px;
		object-fit: cover;
		border-radius: var(--card-radius);
		background: var(--background-tertiary);
		box-shadow: 4px 6px 0 rgba(0, 0, 0, 0.15);
	}

	.about-content {
		display: flex;
		flex-direction: column;
		flex: 1;
		align-items: center;
		justify-content: center;
		gap: 1rem;
		justify-content: flex-start;
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
		min-height: 250px;
		background-color: var(--background-primary);
		padding: 1rem;
		border-radius: var(--card-radius);
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		margin: 0 auto;
		text-align: center;
	}

	.about-text {
		font-family: var(--font-body);
		font-size: 17px;
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
		background: none;
		border: none;
		padding: 0;
		font: inherit;
	}

	.circle-shape {
		width: 150px;
		height: 150px;
		border-radius: 50%;
		border: 3px solid #5a4634;
		background-color: transparent;
		transition: transform 0.2s ease;
		position: relative;
		display: flex;
		align-items: center;
		justify-content: center;
		overflow: hidden;
	}

	.circle-shape img {
		width: 55%;
		height: 55%;
		object-fit: contain;
		pointer-events: none;
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

		.intro-board {
			flex-direction: column;
			align-items: center;
		}

		.sticky-notes {
			display: none;
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

		.profile-image {
			width: 100%;
			max-width: 450px;
			height: auto;
			aspect-ratio: 3 / 4;
			object-fit: cover;
			border-radius: var(--card-radius);
		}

		.about-card {
			order: 2;
			width: 100%;
			max-width: 100%;
			padding: 1rem;
		}

		.about-text {
			font-size: 15px;
		}

		.about-container {
			padding: 0 1rem;
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
