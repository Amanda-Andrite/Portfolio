<script>
//temp to remove warning about unused component
/** @type {{ name: string; path: string }[]} */
	let navigationItems = [];
	let isOpen = false;
</script>

{#if navigationItems.length > 0}
<nav class="nav" aria-label="Main navigation">
    <button
        class="burger"
        on:click={() => (isOpen = !isOpen)}
        aria-label="Toggle navigation menu"
        aria-expanded={isOpen}
        aria-controls="main-menu"
    >
        ☰
    </button>

    <ul id="main-menu" class:open={isOpen}>
        {#each navigationItems as item}
            <li class="nav-item">
                <a href={item.path}>{item.name}</a>
            </li>
        {/each}
    </ul>
</nav>
{/if}

<style>
	.nav {
		display: flex;
		justify-content: flex-end;
		align-items: center;
		width: 100%;
		gap: var(--space-lg);
	}

	.nav ul {
		display: flex;
		flex-wrap: wrap;
		gap: var(--space-md);
		list-style: none;
		margin: 0;
		padding: 0;
	}

	.burger {
		display: none;
	}

	@media (max-width: 768px) {
		.nav {
			flex-direction: column;
			align-items: flex-start;
		}

		.nav ul {
			display: none;
			flex-direction: column;
			gap: var(--space-sm);
			margin-top: var(--space-sm);
		}
	}
</style>
