<footer class="footer">
	<div class="footer-top">
		<div class="footer-left">
			<img src="./icons/logo1.png" alt="Logo" class="footer-logo" />

			<div class="contact">
				<p><strong>Email:</strong> email@email.com</p>
				<p><strong>Phone:</strong> +number</p>
				<p><strong>Insta:</strong> email@email.com</p>
				<p><strong>Twitter:</strong> email@email.com</p>
				<p><strong>LinkedIn:</strong> email@email.com</p>
			</div>
		</div>
	</div>
	<p class="copyright">&copy; 2025 Portfolio. All rights reserved.</p>
</footer>

<style>
	.footer {
		width: 100%;
		padding: 20px 0;
		text-align: left;
		font-family: var(--font-body);
		font-size: var(--font-sm);
		background-color: var(--background-tertiary);
		position: relative;
		z-index: 10;
		flex-direction: column;
		align-items: flex-start;
	}

	.footer::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		height: 15px;
		width: 100%;
		background: var(--divider-color);
	}

	.footer-top {
		width: 100%;
		display: flex;
		justify-content: flex-start;
	}

	.footer-left {
		display: flex;
		gap: 20px;
		align-items: flex-start;
	}

	.footer-logo {
		width: 100px;
		height: 100px;
		object-fit: contain;
		transform: translate(6px, 6px);
	}

	.contact p {
		font-size: 15px;
		color: var(--text-secondary);
		margin: 4px 0;
		transform: translate(6px, 6px);
	}

	.copyright {
		font-size: 13px;
		text-align: center;
		color: var(--text-secondary);
		align-self: flex-end;
	}

	@media (max-width: 768px) {
		.footer {
			flex-direction: column;
			padding: var(--space-sm);
		}

		.footer-logo {
			transform: translate(10px, 15px);
		}

		.contact p {
			font-size: 13px;
		}

		.copyright {
			align-self: flex-start;
            font-size: 10px;
		}
	}
</style>
