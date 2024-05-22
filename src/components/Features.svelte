<!-- src/FeaturesSection.svelte -->
<script>
</script>

<section class="features">
	<h2>Características y Beneficios</h2>
	<div class="feature-row">
		<div class="feature">
			<img src="https://via.placeholder.com/100" alt="Feature 1" />
			<h3>Fácil Inscripción</h3>
			<p>
				Fácil inscripción para ti y tus familiares, garantizando derechohabiencia en caso de
				enfermedades o accidentes.
			</p>
		</div>
		<div class="feature">
			<img src="https://via.placeholder.com/100" alt="Feature 2" />
			<h3>Incapacidad Cubierta</h3>
			<p>
				Incapacidad laboral cubierta, así como prestaciones financieras como jubilación y fondo de
				retiro.
			</p>
		</div>
		<div class="feature">
			<img src="https://via.placeholder.com/100" alt="Feature 3" />
			<h3>Acumulación de Puntos</h3>
			<p>Acumula puntos para el INFONAVIT con nuestro servicio adicional.</p>
		</div>
	</div>
</section>

<style>
	.features {
		padding: 4rem 2rem;
		text-align: center;
	}

	.features h2 {
		font-size: 2rem;
		margin-bottom: 2rem;
	}

	.feature-row {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 2rem;
	}

	.feature {
		flex: 1 1 calc(33.333% - 2rem);
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		padding: 1rem;
		background: #f9f9f9;
		border-radius: 8px;
	}

	.feature img {
		max-width: 100px;
		margin-bottom: 1rem;
	}

	.feature h3 {
		font-size: 1.5rem;
		margin-bottom: 1rem;
	}

	.feature p {
		font-size: 1rem;
	}

	@media (max-width: 768px) {
		.feature {
			flex: 1 1 100%;
		}
	}
</style>
