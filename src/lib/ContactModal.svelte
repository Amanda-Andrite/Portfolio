<script>
	import { contactInfoOpen } from '$lib/stores/contact.js';
</script>

{#if $contactInfoOpen}
	<!--Dark background overlay (click outside to close) -->
	<div
		class="overlay"
		role="button"
		tabindex="0"
		on:click={() => contactInfoOpen.set(false)}
		on:keydown={(e) => e.key === 'Escape' && contactInfoOpen.set(false)}
	>
	<!--Actual Popup of contact card-->
		<div
			class="modal"
			role="dialog"
			aria-modal="true"
			tabindex="0"
			on:keydown={(e) => e.key === 'Escape' && contactInfoOpen.set(false)}
			on:click|stopPropagation
		>
			<h2>Contact Info</h2>
			<h3>Amanda Andrite</h3>
			<p><strong>Email:</strong> email@email.com</p>
			<p><strong>Phone:</strong> +number</p>
			<p><strong>Insta:</strong> email@email.com</p>
			<p><strong>Twitter:</strong> email@email.com</p>
			<p><strong>LinkedIn:</strong> email@email.com</p>
			<button on:click={() => contactInfoOpen.set(false)}> Close </button>
		</div>
	</div>
{/if}

<style>
	.overlay {
		position: fixed;
		inset: 0;
		background: rgba(0, 0, 0, 0.6);
		backdrop-filter: blur(3px);
		display: flex;
		align-items: center;
		justify-content: center;
		z-index: 9999;
	}

	.modal {
		background: var(--background-primary);
		padding: var(--space-lg);
		border-radius: var(--card-radius);
		width: 320px;
		box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
		text-align: center;
		animation: popIn 0.2s ease;
	}

	button {
		margin-top: var(--space-md);
		padding: 0.5rem 1rem;
		background: var(--color-button);
		color: var(--text-secondary);
		border: none;
		border-radius: var(--radius-sm);
		cursor: pointer;
	}

	@keyframes popIn {
		from {
			transform: scale(0.9);
			opacity: 0;
		}
		to {
			transform: scale(1);
			opacity: 1;
		}
	}
</style>
