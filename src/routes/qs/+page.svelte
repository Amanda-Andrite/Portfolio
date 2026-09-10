<script>
	// @ts-nocheck
	let qa = [
		{
			question: 'What kind of work do you focus on?',
			answer:
				'I mainly explore wireframing, concept art, and occasioanlly 3D visuals. I enjoy creating immersive experiences and exploring new ways to communicate ideas through design, which is why I feel in love with designing wireframes and creating design concepts that are both modern and visually appealing, whilst keeping designs up to date.',
			open: false
		},
		{
			question: 'How would you describe your design style in Wireframing?',
			answer:
				'Clean, structured, and calm. I try to avoid anything that feels overwhelming and instead focus on clarity and flow.',
			open: false
		},
		{
			question: 'What tools do you use?',
			answer:
				'I switch between design and 3D tools depending on the project. I like using whatever best helps me communicate the idea clearly. For wireframing, I use Figma or Penpot. For concept art, I use Krita. For 3D visuals, Ive grown fond of Blender, but have dabbled in using Maya.',
			open: false
		},
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
				<div class="answer-wrap {item.open ? 'open' : ''}">
					<div class="answer">
						{item.answer}
					</div>
				</div>
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
		transition:
			transform 0.2s ease,
			box-shadow 0.2s ease;
	}

	.question:hover {
		transform: scale(1.01);
		box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
	}

	.icon {
		font-size: 1.5rem;
	}

	.answer-wrap {
		max-height: 0;
		overflow: hidden;
		transform: translateY(-5px);
		transition: transform 0.55s ease;
	}

	.answer-wrap.open {
		max-height: 200px;
		opacity: 1;
		transform: translateY(0);
		margin-top: 0rem;
	}

	.answer {
		background: var(--background-secondary);
		padding: var(--card-padding);
		border-radius: var(--card-radius);
		color: var(--text-primary);
	}

	@media (max-width: 768px) {
		.grid {
			grid-template-columns: 1fr;
		}
	}
</style>
