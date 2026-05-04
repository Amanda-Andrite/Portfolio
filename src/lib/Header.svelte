<script>
	import { resolve } from '$app/paths';
	import { contactInfoOpen } from '$lib/stores/contact.js';
	import { base } from '$app/paths';

	//Issues with trying to import pages, so active link state is handled manually instead
	let activeLink = '';
</script>

<header class="header">
	<nav class="nav-bar">
		<div class="nav-left">
			<a
				href={resolve('/skills')}
				class:active={activeLink === '/skills'}
				on:click={() => (activeLink = '/skills')}
			>
				My Skills
			</a>
			<a
				href="#top"
				on:click|preventDefault={() => {
					contactInfoOpen.set(true);
					activeLink = 'contacts';
				}}
				class:active={activeLink === 'contacts'}
			>
				Contacts
			</a>
		</div>
		<div class="logo">
			<a href={resolve('/')} on:click={() => (activeLink = '/')} class:active={activeLink === '/'}>
				<img src="{base}/icons/logo1.png" alt="Logo" />
			</a>
		</div>
		<div class="nav-right">
			<a
				href={resolve('/work')}
				on:click={() => (activeLink = '/work')}
				class:active={activeLink === '/work'}
				>My Work
			</a>

			<a
				href={resolve('/qs')}
				on:click={() => (activeLink = '/qs')}
				class:active={activeLink === '/qs'}
			>
				QA
			</a>
		</div>
	</nav>
</header>

<style>
	.header {
		width: fit-content;
		margin: 0 auto;
		position: relative;
		top: 0;
	}

	.nav-bar {
		width: 100%;
		height: 60px;
		background-color: var(--background-secondary);
		border-left: 2px dashed var(--background-tertiary);
		border-right: 2px dashed var(--background-tertiary);
		border-bottom: 2px dashed var(--background-tertiary);
		border-radius: 10px;
		display: flex;
		align-items: center;
		gap: 2rem;
		padding: 1rem 2rem;
	}

	.nav-left,
	.nav-right {
		display: flex;
		gap: 1.5rem;
	}

	.logo img {
		width: 50px;
		height: 50px;
		object-fit: contain;
		display: block;
		transform: translateY(3px);
	}

	.nav-bar a {
		position: relative;
		display: inline-block;
		text-decoration: none;
		color: var(--text-primary);
		font-family: var(--font-button);
		font-size: 1.1rem;
		padding: 0.3rem 0.6rem;
		border-radius: 999px;
		transition: all 0.2s ease;
	}

	.nav-bar a:hover {
		transform: scale(1.1);
	}

	.logo a:hover {
		transform: scale(1.1);
	}

	.nav-bar a.active {
		color: #ffff;
		background-color: var(--background-tertiary);
	}

	.nav-bar a.active::before {
		position: absolute;
		background-color: var(--background-tertiary);
		border-radius: 90px;
	}

	@media (max-width: 768px) {
		.header {
			transform: scale(0.85);
			transform-origin: top center;
		}

		.nav-bar {
			gap: 1.2rem;
			padding: 0.8rem 1rem;
		}

		.nav-left,
		.nav-right {
			gap: 0.8rem;
		}

		.logo img {
			margin: 0 0.8rem;
		}

		.nav-bar a {
			font-size: 0.95rem;
		}
	}
</style>
