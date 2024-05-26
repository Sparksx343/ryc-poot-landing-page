<footer>
	<div class="footer-content">
		<div class="social-links">
			<a href="https://facebook.com" target="_blank" aria-label="Facebook">
				<i class="fab fa-facebook"></i>
			</a>
			<a href="https://twitter.com" target="_blank" aria-label="Twitter">
				<i class="fab fa-twitter"></i>
			</a>
			<a href="https://instagram.com" target="_blank" aria-label="Instagram">
				<i class="fab fa-instagram"></i>
			</a>
			<a href="tel:529613731566" target="_blank" aria-label="WhatsApp">
				<i class="fab fa-whatsapp"></i>
			</a>
            <a href="https://tiktok.com" target="_blank" aria-label="TikTok">
				<i class="fab fa-tiktok"></i>
			</a>
		</div>
		<div class="footer-links">
			<a href="/about">Acerca</a>
			<a href="/services">Servicios</a>
			<a href="#privacy">Privacidad</a>
			<a href="#terms">Términos</a>
			<a href="#contact">Contacto</a>
		</div>
	</div>
	<p>&copy; {new Date().getFullYear()} RyC. Todos los derechos reservados.</p>
</footer>

<style>
	footer {
		background-color: #282c34;
		color: white;
		padding: 2rem 1rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		text-align: center;
		box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
	}

	.footer-content {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 1rem;
	}

	.social-links {
		display: flex;
		gap: 1rem;
	}

	.social-links a {
		color: white;
		text-decoration: none;
		font-size: 1.5rem;
		transition: transform 0.3s ease;
	}

	.social-links a:hover {
		transform: scale(1.2);
	}

	.footer-links {
		display: flex;
		gap: 1rem;
		flex-wrap: wrap;
		justify-content: center;
	}

	.footer-links a {
		color: white;
		text-decoration: none;
		transition: color 0.3s ease;
	}

	.footer-links a:hover {
		color: #4b6cb7;
	}

	@media (min-width: 768px) {
		.footer-content {
			flex-direction: row;
			justify-content: space-between;
			width: 80%;
		}
	}
</style>