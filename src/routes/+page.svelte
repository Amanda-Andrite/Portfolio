<script>
</script>

<svelte:head>
	<title>Portfolio</title>
</svelte:head>

<main class="page">
	<section class="intro">
		<div class="intro-content">
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
</style>
