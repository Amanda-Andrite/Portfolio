<script>
//empty
</script>

<header class="header">
	<nav class="nav-bar">
		<div class="nav-left">
			<a href="skills">My Skills</a>
			<a href="contacts">Contacts</a>
		</div>
		<div class="logo">
			<p> Logo </p>
		</div>
		<div class="nav-right">
			<a href="work">My Work</a>
			<a href="qa">Q/A</a>
		</div>
	</nav>
</header>

<style>
	.header {
		width: fit-content;
		margin: 0 auto;
	}

	.nav-bar {
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
