<script>
	let items = [
		{ title: 'Wireframes & UX', type: 'left' },
		{ title: 'Concept Art & Worlds', type: 'center' },
		{ title: '3D Exploration', type: 'right' }
	];
</script>

<div class="page">
	<h1>My Work</h1>
	<div class="grid">
		{#each items as item}
			<div class="polaroid {item.type}">
				<div class="frame"></div>
				<p>{item.title}</p>
			</div>
		{/each}
	</div>
</div>

<style>
	.page {
		min-height: 100vh;
		padding: 3rem;
		background: var(--background-primary);
		font-family: system-ui, sans-serif;
		text-align: center;
	}

	h1 {
		font-size: 3rem;
		margin-bottom: 3rem;
		color: var(--text-primary);
	}

	.grid {
		display: flex;
		justify-content: center;
		align-items: flex-start;
		gap: 2.5rem;
	}

	.polaroid {
		background: #ffff;
		padding: 1rem 1rem 1.5rem 1rem;
		width: 220px;
		box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
	}

	.frame {
		background: var(--background-tertiary);
		padding: 0.5rem;
		height: 200px;
	}

	p {
		margin-top: 1rem;
		font-weight: bold;
		color: var(--text-primary)
	}
</style>
