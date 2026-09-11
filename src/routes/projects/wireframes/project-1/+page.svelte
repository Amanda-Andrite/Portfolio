<script>
	import { resolve, base } from '$app/paths';
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

	<!--Low Fidelity -->
	<section class="section">
		<h2>Sketches of Low-Fidelity Wireframes</h2>
		<p>
			I began by sketching out initial ideas and exploring different layouts for the application. I
			first considered the target audience and decided to design the application around the needs of
			a college student with a busy schedule.
		</p>
		<div class="image-grid">
			<div class="image-placeholder"></div>
			<div class="image-placeholder"></div>
			<div class="image-placeholder"></div>
		</div>
	</section>

	<!-- Medium Fidelity -->
	<section class="section">
		<h2>Medium-Fidelity Wireframes</h2>
		<div class="image-grid">
			<img
				src={`${base}/imgs/lowFidelity_Desktop_SignUp.png`}
				alt="User journey flow diagram for the To-Do List App"
				class="image-large"
			/>
			<img
				src={`${base}/imgs/lowFidelity_Desktop_Homepage.png`}
				alt="User journey flow diagram for the To-Do List App"
				class="image-large"
			/>
			<img
				src={`${base}/imgs/lowFidelity_Desktop_Board.png`}
				alt="User journey flow diagram for the To-Do List App"
				class="image-large"
			/>
		</div>
		<div class="mobile-grid">
			<img
				src={`${base}/imgs/lowFidelity_Mobile_SignUp.png`}
				alt="User journey flow diagram for the To-Do List App"
				class="mobile-image"
			/>
			<img
				src={`${base}/imgs/lowFidelity_Mobile_Homepage.png`}
				alt="User journey flow diagram for the To-Do List App"
				class="mobile-image"
			/>
			<img
				src={`${base}/imgs/lowFidelity_Mobile_Board.png`}
				alt="User journey flow diagram for the To-Do List App"
				class="mobile-image"
			/>
			<img
				src={`${base}/imgs/lowFidelity_Mobile_Panel.png`}
				alt="User journey flow diagram for the To-Do List App"
				class="mobile-image"
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
		<div class="image-grid">
			<div class="image-placeholder"></div>
			<div class="image-placeholder"></div>
			<div class="image-placeholder"></div>
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
		<div class="final-design"></div>
	</section>
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

	.image-placeholder {
		min-height: 250px;
		background: white;
		border-radius: var(--card-radius);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.18);
	}

	.final-design {
		width: 100%;
		min-height: 500px;
		background: white;
		border-radius: var(--card-radius);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.18);
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
