<script>
	import { base } from '$app/paths';
	let items = [
		{ title: 'Wireframes & UX', type: 'left', link: '/projects/wireframes' },
		{ title: 'Concept Art & Worlds', type: 'center', link: '/projects/concept' },
		{ title: '3D Exploration', type: 'right', link: '/projects/models' }
	];
</script>

<div class="page">
	<h1>My Work</h1>
	<div class="grid">
		{#each items as item}
			<a class="link" href="{base}{item.link}">
				<div class="polaroid {item.type}">
					<div class="frame"></div>
					<p>{item.title}</p>
				</div>
			</a>
		{/each}
	</div>
</div>

<style>
	.page {
		min-height: 100vh;
		padding: var(--space-lg);
		background: var(--background-primary);
		font-family: var(--font-body);
		text-align: center;
	}

	h1 {
		font-size: 3rem;
		margin-bottom: var(--space-lg);
		color: var(--text-primary);
		font-family: var(--font-heading);
	}

	.grid {
		display: flex;
		justify-content: center;
		align-items: flex-start;
		gap: var(--gap-lg);
	}

	.polaroid {
		background: #ffff;
		padding: var(--card-padding);
		width: 270px;
		height: 330px;
		box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
		transition: transform 0.55s ease;
	}

	.polaroid:hover {
		transform: translateY(-8px);
		box-shadow: 0 18px 40px rgba(0, 0, 0, 0.2);
	}

	.frame {
		background: var(--background-tertiary);
		padding: 0.5rem;
		height: 250px;
	}

	p {
		margin-top: var(--space-md);
		font-weight: bold;
		color: var(--text-primary);
		font-family: var(--font-button);
	}

	.left {
		transform: rotate(-3deg);
	}

	.right {
		transform: rotate(3deg);
	}

	.center {
		transform: translateY(40px);
	}

	.link {
		text-decoration: none;
		color: inherit;
	}

	@media (max-width: 768px) {
		.grid {
			flex-direction: column;
			align-items: center;
			gap: var(--space-lg);
		}

		.polaroid {
			width: 240px;
			height: 290px;
			transition: transform 0.55s ease;
		}

		.frame {
			height: 200px;
		}

		.left {
			transform: rotate(-2deg) translateX(-30px);
		}

		.right {
			transform: rotate(-2deg) translateX(-30px);
		}

		.center {
			transform: rotate(2deg) translateX(30px);
		}

		.polaroid:hover {
			transform: translateY(-6px);
		}
	}
</style>
