<script>
	let items = ['Project 1', 'Project 2', 'Project 3', 'Project 4', 'Project 5', 'Project 6'];
</script>

<div class="page">
	<h1>Wireframes & UX</h1>
	<div class="grid">
		{#each items as item}
			<div class="card">
				{item}
			</div>
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
		color: var(--text-primary);
	}

	h1 {
		font-size: 3rem;
		margin-bottom: var(--space-lg);
		font-family: var(--font-heading);
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
		gap: var(--gap-lg);
		max-width: 900px;
		margin: 0 auto;
	}

	.card {
		height: 120px;
		background: white;
		border-radius: var(--card-radius);
		display: flex;
		align-items: center;
		justify-content: center;
        font-family: var(--font-button);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.18);
		transition: transform 0.2s ease;
	}

	.card:hover {
		transform: translateY(-5px);
        box-shadow: 0 14px 28px rgba(0, 0, 0, 0.18);
	}
</style>