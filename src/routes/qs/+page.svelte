<script>
	// @ts-nocheck
	let qa = [
		{ question: 'question1', answer: '----- Text -----', open: false },
		{ question: 'question2', answer: '----- Text -----', open: false },
		{ question: 'question3', answer: '----- Text -----', open: false },
		{ question: 'question4', answer: '----- Text -----', open: false },
		{ question: 'question5', answer: '----- Text -----', open: false },
		{ question: 'question6', answer: '----- Text -----', open: false }
	];

	function toggle(index) {
		qa = qa.map((item, i) => (i === index ? { ...item, open: !item.open } : item));
	}
</script>

<div class="page">
	<h1>Learn About Me</h1>
	<div class="divider"></div>
	<div class="grid">
		{#each qa as item, i}
			<div class="qa">
				<button class="question" on:click={() => toggle(i)}>
					<span>{item.question}</span>
					<span class="icon">{item.open ? '-' : '+'}</span>
				</button>
				{#if item.open}
					<div class="answer">
						{item.answer}
					</div>
				{/if}
			</div>
		{/each}
	</div>
</div>

<style>
	.page {
		padding: var(--space-lg);
		background: var(--background-primary);
		min-height: 100vh;
		font-family: var(--font-body);
		color: var(--text-primary);
	}

	h1 {
		text-align: center;
		font-family: var(--font-heading);
		font-size: 3rem;
		margin-bottom: var(--space-md);
	}

	.divider {
		height: 2px;
		background: var(--divider-color);
		margin-bottom: var(--space-lg);
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: var(--gap-lg);
	}

	.qa {
		width: 100%;
	}

	.question {
		background: var(--background-tertiary);
		color: var(--text-secondary);
		padding: var(--card-padding);
		border-radius: var(--card-radius);
		display: flex;
		justify-content: space-between;
		align-items: center;
		cursor: pointer;
		font-weight: bold;
		border: none;
		width: 100%;
		text-align: left;
	}

	.icon {
		font-size: 1.5rem;
	}

	.answer {
		background: var(--background-secondary);
		padding: var(--card-padding);
		border-radius: var(--card-radius);
		margin-top: 0;
		color: var(--text-primary);
	}

	@media (max-width: 768px) {
		.grid {
			grid-template-columns: 1fr;
		}
	}
</style>
