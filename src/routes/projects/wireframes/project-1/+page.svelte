<script>
	import { resolve, base } from '$app/paths';
	let selectedImage = '';

	let finalDesigns = [
		`${base}/imgs/high-Fidelity(Desktop)Intro-3.png`,
		`${base}/imgs/high-Fidelity(Desktop)SignUp-3.png`,
		`${base}/imgs/high-Fidelity(Desktop)Login-3.png`,
		`${base}/imgs/high-Fidelity(Desktop)Homepage2-3.png`,
		`${base}/imgs/high-Fidelity(Desktop)ManageAccount-3.png`,
		`${base}/imgs/high-Fidelity(Desktop)Settings-3.png`,
		`${base}/imgs/high-Fidelity(Desktop)Boards-3.png`,
		`${base}/imgs/high-Fidelity(Desktop)Board-3.png`,
		`${base}/imgs/high-Fidelity(Desktop)AddTask2-3.png`,
		`${base}/imgs/high-Fidelity(Desktop)EditTask-3.png`
	];

	let currentFinal = 0;

	function nextFinal() {
		currentFinal = (currentFinal + 1) % finalDesigns.length;
	}

	function previousFinal() {
		currentFinal = (currentFinal - 1 + finalDesigns.length) % finalDesigns.length;
	}
</script>

<div class="page">
	<!--back button -->
	<a href={resolve('/projects/wireframes')} class="back"> Back to Wireframes & UX </a>

	<h1>To-Do List Application</h1>
	<section class="section">
		<h2>Description</h2>
		<p>
			This project is a To-Do List application designed to help users create, manage, and organise
			their tasks efficiently. The application allows users to add, edit, complete, and delete tasks
			through a simple and intuitive interface.
		</p>

		<div>
			<h2>Purpose for Project</h2>
			<p>
				This project was created as part of my college coursework for a Wireframing module, focusing
				on the planning and development of a user-friendly application interface on both Desktop and
				Mobile.
			</p>
		</div>

		<div>
			<h2>Tools Used</h2>
			<div class="tools">
				<span>Penpot</span>
				<span>Draw.io</span>
			</div>
		</div>
	</section>

	<!-- User Journey -->
	<section class="section">
		<h1>User Journey</h1>
		<img
			src={`${base}/imgs/FlowDiagram.drawio1.png`}
			alt="User journey flow diagram for the To-Do List App"
			class="image-large"
		/>
	</section>

	<!-- Medium Fidelity -->
	<section class="section">
		<h2>Medium-Fidelity Wireframes</h2>
		<p>
			I began by sketching out initial ideas and exploring different layouts for the application. I
			first considered the target audience and decided to design the application around the needs of
			a college student with a busy schedule.
		</p>
		<div class="image-grid">
			<img
				src={`${base}/imgs/mediumFidelity_Desktop_SignUp.png`}
				alt="Medium fidelity wireframe for the Sign-Up page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/mediumFidelity_Desktop_SignUp.png`)}
			/>
			<img
				src={`${base}/imgs/mediumFidelity_Desktop_Homepage.png`}
				alt="Medium fidelity wireframe for the Home page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/mediumFidelity_Desktop_Homepage.png`)}
			/>
			<img
				src={`${base}/imgs/mediumFidelity_Desktop_Board.png`}
				alt="Medium fidelity wireframe for the Board page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/mediumFidelity_Desktop_Board.png`)}
			/>
		</div>
		<div class="mobile-grid">
			<img
				src={`${base}/imgs/mediumFidelity_Mobile_SignUp.png`}
				alt="Medium fidelity wireframe for the Sign-Up page of the To-Do List App"
				class="mobile-image"
				onclick={() => (selectedImage = `${base}/imgs/mediumFidelity_Mobile_SignUp.png`)}
			/>
			<img
				src={`${base}/imgs/mediumFidelity_Mobile_Homepage.png`}
				alt="Medium fidelity wireframe for the Home page of the To-Do List App"
				class="mobile-image"
				onclick={() => (selectedImage = `${base}/imgs/mediumFidelity_Mobile_Homepage.png`)}
			/>
			<img
				src={`${base}/imgs/mediumFidelity_Mobile_Board.png`}
				alt="Medium fidelity wireframe for the Board page of the To-Do List App"
				class="mobile-image"
				onclick={() => (selectedImage = `${base}/imgs/mediumFidelity_Mobile_Board.png`)}
			/>
			<img
				src={`${base}/imgs/mediumFidelity_Mobile_Panel.png`}
				alt="Medium fidelity wireframe for the Panel page of the To-Do List App"
				class="mobile-image"
				onclick={() => (selectedImage = `${base}/imgs/mediumFidelity_Mobile_Panel.png`)}
			/>
		</div>
	</section>

	<!-- High Fidelity -->
	<section class="section">
		<h2>High-Fidelity Wireframes</h2>
		<p>
			At this stage, I explored different colour palettes and visual styles to determine what would
			work best for the application. I wanted the design to remain clean and intuitive while still
			being visually appealing.
		</p>
		<div class="high-fidelity-row single">
			<img
				src={`${base}/imgs/high-Fidelity(Desktop)Intro-1.png`}
				alt="High fidelity wireframe for the Intro page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/high-Fidelity(Desktop)Intro-1.png`)}
			/>
			<img
				src={`${base}/imgs/high-Fidelity(Desktop)SignUp-1.png`}
				alt="High fidelity wireframe for the Sign-Up page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/high-Fidelity(Desktop)SignUp-1.png`)}
			/>
			<img
				src={`${base}/imgs/high-Fidelity(Desktop)Homepage-1.png`}
				alt="High fidelity wireframe for the Home page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/high-Fidelity(Desktop)Homepage-1.png`)}
			/>
		</div>
		<div class="high-fidelity-row">
			<img
				src={`${base}/imgs/high-Fidelity(Desktop)Intro-2.png`}
				alt="High fidelity wireframe for the Intro page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/high-Fidelity(Desktop)Intro-2.png`)}
			/>
			<img
				src={`${base}/imgs/high-Fidelity(Desktop)SignUp-2.png`}
				alt="High fidelity wireframe for the Sign-Up page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/high-Fidelity(Desktop)SignUp-2.png`)}
			/>
			<img
				src={`${base}/imgs/high-Fidelity(Desktop)Homepage-2.png`}
				alt="High fidelity wireframe for the Home page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/high-Fidelity(Desktop)Homepage-2.png`)}
			/>
		</div>
		<div class="high-fidelity-row">
			<img
				src={`${base}/imgs/high-Fidelity(Desktop)Intro-3.png`}
				alt="High fidelity wireframe for the Intro page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/high-Fidelity(Desktop)Intro-3.png`)}
			/>
			<img
				src={`${base}/imgs/high-Fidelity(Desktop)SignUp-3.png`}
				alt="High fidelity wireframe for the Sign-Up page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/high-Fidelity(Desktop)SignUp-3.png`)}
			/>
			<img
				src={`${base}/imgs/high-Fidelity(Desktop)Homepage-3.png`}
				alt="High fidelity wireframe for the Home page of the To-Do List App"
				class="image-large"
				onclick={() => (selectedImage = `${base}/imgs/high-Fidelity(Desktop)Homepage-3.png`)}
			/>
		</div>
	</section>

	<!-- Final Designs -->
	<section class="section">
		<h2>Final Designs</h2>
		<p>
			For the final design, I chose an earthy brown colour palette to create a calmer and more
			focused experience. The intention was to make the application feel approachable and organised,
			helping tasks feel simple and achievable rather than overwhelming.
		</p>
		<div class="final-design">
			<button class="arrow left" onclick={previousFinal} aria-label="Previous final design">
				🠸
			</button>
			<img
				src={finalDesigns[currentFinal]}
				alt="Final To-Do List App wireframe"
				class="final-image"
				onclick={() => (selectedImage = finalDesigns[currentFinal])}
			/>
			<button class="arrow right" onclick={nextFinal} aria-label="Next final design"> 🠺 </button>
		</div>

		<div class="pdf-buttons">
			<a
				href={`${base}/pdfs/Desktop-(High Fidelity).pdf`}
				target="_blank"
				rel="noopener noreferrer"
				class="pdf-button"
			>
				View Desktop Wireframes
			</a>

			<a
				href={`${base}/pdfs/Mobile-(High Fidelity).pdf`}
				target="_blank"
				rel="noopener noreferrer"
				class="pdf-button"
			>
				View Mobile Wireframes
			</a>
		</div>
	</section>

	{#if selectedImage}
		<div class="lightbox" onclick={() => (selectedImage = '')}>
			<img
				src={selectedImage}
				alt="Enlarged wireframe"
				onclick={(event) => event.stopPropagation()}
			/>

			<button onclick={() => (selectedImage = '')} aria-label="Close image"> x </button>
		</div>
	{/if}
</div>

<style>
	.page {
		min-height: 100vh;
		padding: var(--space-sm);
		background: var(--background-primary);
		font-family: var(--font-body);
		color: var(--text-primary);
	}

	.back {
		display: inline-block;
		margin-bottom: 50px;
		color: var(--text-primary);
		text-decoration: none;
		font-family: var(--font-button);
	}

	.back:hover {
		text-decoration: underline;
	}

	h1 {
		font-family: var(--font-heading);
		font-size: 3rem;
		text-align: center;
		margin: 0 0 25px 0;
	}

	.section {
		max-width: 900px;
		margin: 0 auto 55px auto;
	}

	h2 {
		font-family: var(--font-heading);
		font-size: 1.8rem;
		margin: 0 0 15px 0;
	}

	p {
		font-size: 1.05rem;
		line-height: 1.6;
		max-width: 750px;
	}

	.image-large {
		width: 65%;
		height: auto;
		display: block;
		margin: 0 auto;
		background: white;
		border-radius: var(--card-radius);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.18);
	}

	.image-grid .image-large {
		width: 105%;
	}

	.image-grid {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: var(--gap-lg);
	}

	.mobile-grid {
		display: flex;
		justify-content: center;
		align-items: flex-start;
		gap: 30px;
		margin-top: 40px;
		flex-wrap: wrap;
	}

	.mobile-image {
		width: 150px;
		height: auto;
		display: block;
		background: white;
		border-radius: var(--card-radius);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.18);
	}

	.high-fidelity-row {
		display: flex;
		justify-content: center;
		align-items: flex-start;
		gap: 30px;
		margin-top: 30px;
	}

	.high-fidelity-row img {
		width: 30%;
		height: auto;
		display: block;
		background: white;
		border-radius: var(--card-radius);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.18);
		cursor: pointer;
	}

	.high-fidelity-row.single img {
		width: 30%;
	}

	.final-design {
		position: relative;
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 25px;
		margin-top: 30px;
	}

	.final-image {
		width: 65%;
		height: auto;
		display: block;
		background: white;
		border-radius: var(--card-radius);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.18);
		cursor: pointer;
	}

	.arrow {
		width: 50px;
		height: 50px;
		border: none;
		border-radius: 50%;
		background: white;
		font-size: 2rem;
		cursor: pointer;
		display: flex;
		align-items: center;
		justify-content: center;
		box-shadow: 0 5px 15px rgba(0, 0, 0, 0.18);
		flex-shrink: 0;
	}

	.arrow:hover {
		transform: scale(1.1);
	}

	.arrow:active {
		transform: scale(0.95);
	}

	.tools {
		display: flex;
		gap: 15px;
		flex-wrap: wrap;
	}

	.tools span {
		background: white;
		padding: 10px 18px;
		border-radius: 20px;
		font-family: var(--font-button);
		box-shadow: 0 5px 12px rgba(0, 0, 0, 0.12);
	}

	.image-large,
	.mobile-image {
		cursor: pointer;
	}

	.lightbox {
		position: fixed;
		inset: 0;
		background: rgba(0, 0, 0, 0.75);
		display: flex;
		align-items: center;
		justify-content: center;
		padding: 40px;
		z-index: 1000;
	}

	.lightbox img {
		max-width: 90%;
		max-height: 90vh;
		width: auto;
		height: auto;
		object-fit: contain;
		background: white;
		border-radius: var(--card-radius);
		box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
	}

	.lightbox button {
		position: absolute;
		top: 20px;
		right: 30px;
		background: white;
		border: none;
		border-radius: 50%;
		width: 45px;
		height: 45px;
		font-size: 2rem;
		cursor: pointer;
		line-height: 1;
	}

	.pdf-buttons {
		display: flex;
		justify-content: center;
		gap: 20px;
		margin-top: 35px;
	}

	.pdf-button {
		display: block;
		width: 220px;
		padding: 15px 20px;
		background: rgba(62, 47, 29, 0.941);
		color: rgb(247, 230, 215);
		text-align: center;
		text-decoration: none;
		border-radius: var(--card-radius);
		font-family: var(--font-button);
		box-shadow: 0 5px 12px rgba(0, 0, 0, 0.15);
	}

	.pdf-button:hover {
		transform: translateY(-3px);
		box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
	}

	@media (max-width: 700px) {
		.page {
			padding: var(--space-md);
		}

		h1 {
			font-size: 3rem;
		}

		h2 {
			font-size: 1.8rem;
		}

		.image-grid {
			grid-template-columns: 1fr;
		}
	}
</style>
