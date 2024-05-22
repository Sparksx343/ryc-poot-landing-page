<!-- src/PricingSection.svelte -->
<script>
</script>

<section class="pricing">
	<h2>Planes y Precios</h2>
	<div class="plan">
		<h3>Plan Básico</h3>
		<p>$100/mes</p>
		<p>Incluye todos los beneficios básicos del IMSS</p>
		<button>Seleccionar</button>
	</div>
	<div class="plan">
		<h3>Plan Premium</h3>
		<p>$150/mes</p>
		<p>Incluye beneficios adicionales y acumulación de puntos para el INFONAVIT</p>
		<button>Seleccionar</button>
	</div>
</section>

<style>
	.pricing {
		padding: 4rem 2rem;
		text-align: center;
	}

	.pricing h2 {
		font-size: 2rem;
		margin-bottom: 2rem;
	}

	.pricing .plan {
		background-color: white;
		padding: 2rem;
		border-radius: 5px;
		box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
		margin-bottom: 2rem;
	}

	.pricing .plan h3 {
		font-size: 1.5rem;
		margin-bottom: 1rem;
	}

	.pricing .plan p {
		font-size: 1rem;
		margin-bottom: 1rem;
	}

	.pricing .plan button {
		background-color: #ff4081;
		color: white;
		border: none;
		padding: 1rem 2rem;
		font-size: 1rem;
		border-radius: 5px;
		cursor: pointer;
		transition: background-color 0.3s ease;
	}

	.pricing .plan button:hover {
		background-color: #e00070;
	}

	@media (max-width: 768px) {
		.pricing .plan {
			margin: 0 1rem 2rem;
		}
	}
</style>
