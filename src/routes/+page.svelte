<script>
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
			<button>Contact Me</button>
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
	}

	.image-placeholder {
		width: 450px;
		height: 580px;
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
</style>
