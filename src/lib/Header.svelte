<script>
	import { resolve } from '$app/paths';
</script>

<header class="header">
	<nav class="nav-bar">
		<div class="nav-left">
			<a href={resolve('/skills')}>My Skills</a>
			<a href={resolve('/contact')}>Contacts</a>
		</div>
		<div class="logo">
			<a href={resolve('/')}>Logo</a>
		</div>
		<div class="nav-right">
			<a href={resolve('/work')}>My Work</a>
			<a href={resolve('/qs')}>Q/A</a>
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

	.logo {
		margin: 0 2rem;
		font-size: 1.5rem;
	}

	.nav-bar a {
		text-decoration: none;
		color: var(--text-primary);
		font-family: var(--font-button);
		font-size: 1.1rem;
	}
</style>
