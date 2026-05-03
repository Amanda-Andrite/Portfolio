<script>
	//data for skills page
	const skills = [
		'Visual Studio Code',
		'Adobe Photoshop',
		'GitHub',
		'Blender',
		'JavaScript',
		'C++',
		'Figma'
	];
</script>

<section class="skills">
	<h2>Tools I Use</h2>
	<div class="divider"></div>
	<div class="grid">
		{#each skills as skill}
			<div class="card" role="button" tabindex="0">
				<div class="image-box"></div>
				<div class="name">{skill}</div>
			</div>
		{/each}
	</div>

	<div class="primary-divider"></div>
	<div class="secondary-divider"></div>
</section>

<style>
	.skills {
		padding: var(--space-sm);
		text-align: center;
		padding-bottom: var(--space-lg);
	}

	h2 {
		font-size: 2.5rem;
		margin-bottom: var(--space-md);
		font-family: var(--font-heading);
		color: var(--text-primary);
	}

	.divider {
		height: 2px;
		background: var(--divider-color);
		margin-bottom: var(--space-lg);
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(4, 260px);
		gap: var(--gap-lg);
		justify-content: center;
		margin-bottom: var(--space-lg);
	}

	.card {
		position: relative;
		background: var(--background-secondary);
		padding: var(--card-padding);
		border-radius: var(--card-radius);
		width: 220px;
		height: 270px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
	}

	.image-box {
		width: 100%;
		height: 230px;
		background: var(--background-primary);
		border-radius: var(--radius-md);
	}

	.name {
		font-family: var(--font-button);
		color: var(--text-primary);
		font-weight: bold;
		text-align: center;
		font-size: var(--font-md);
		margin-top: var(--space-sm);
	}

	.primary-divider {
		height: 30px;
		background-color: var(--background-tertiary);
		margin: 0;
	}

	.secondary-divider {
		height: 300px;
		background-color: var(--background-secondary);
		margin: 0;
	}

	@media (max-width: 600px) {
		.grid {
			grid-template-columns: repeat(2, 1fr);
			gap: var(--space-md);
			padding: 0 var(--space-sm);
		}

		.card {
			width: 100%;
			max-width: 220px;
			height: 240px;
			margin: 0 auto;
		}

		.image-box {
			height: 180px;
		}

		.name {
			font-size: 1rem;
		}
	}
</style>
