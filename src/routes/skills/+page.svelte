<script>
	import { base } from '$app/paths';

	//data for skills page
	const skills = [
		{ name: 'Visual Studio Code', img: `${base}/imgs/vscode.png` },
		{ name: 'Adobe Photoshop', img: `${base}/imgs/adobe.png` },
		{ name: 'GitHub', img: `${base}/imgs/github.png` },
		{ name: 'Blender', img: `${base}/imgs/blender.png` },
		{ name: 'Figma', img: `${base}/imgs/figma.png` }
	];
</script>

<section class="skills">
	<h2>Tools I Use</h2>
	<div class="divider"></div>
	<div class="grid">
		{#each skills as skill}
			<div class="card" role="button" tabindex="0">
				<div class="image-box">
					<img src={skill.img} alt={skill.name} />
				</div>
				<div class="name">{skill.name}</div>
			</div>
		{/each}
	</div>
	<div class="section-divider"></div>
	<section class="qualifications">
		<h2>Qualifications</h2>
		<div class="divider"></div>

		<div class="qualification-list">
			<div class="qualification-box">Game Design: Practical Unity Development - FutureLearn</div>
		</div>
	</section>
</section>

<style>
	.skills {
		background: var(--background-primary);
		padding: var(--space-sm) 0;
		text-align: center;
	}

	.qualifications {
		background: var(--background-secondary);
		padding: var(--space-md);
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
		transition:
			transform 0.25s ease,
			box-shadow 0.25s ease;
	}

	.card:hover {
		transform: scale(1.01);
		box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
	}

	.image-box {
		width: 100%;
		height: 230px;
		background: var(--background-primary);
		border-radius: var(--radius-md);
		overflow: hidden;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.image-box img {
		width: 70%;
		height: 70%;
		object-fit: contain;
		transition: transform 0.3s ease;
	}

	.name {
		font-family: var(--font-button);
		color: var(--text-primary);
		font-weight: bold;
		text-align: center;
		font-size: var(--font-md);
		margin-top: var(--space-sm);
	}

	.section-divider {
		height: 30px;
		background-color: var(--divider-color);
		margin: 0;
	}

	.qualification-list {
		display: flex;
		flex-direction: column;
		gap: 15px;
		align-items: center;
	}

	.qualification-box {
		background: white;
		padding: 10px 15px;
		border-radius: 8px;
		width: 60%;
		text-align: center;
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
