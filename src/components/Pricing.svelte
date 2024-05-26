<!-- src/PricingSection.svelte -->
<script>
</script>

<section class="pricing">
	<h2>Planes y Precios</h2>
	<div class="plan-container">
		<div class="plan">
			<h3>Plan Básico</h3>
			<p class="price">$100/mes</p>
			<p>Incluye todos los beneficios básicos del IMSS</p>
			<button>Seleccionar</button>
		</div>
		<div class="plan">
			<h3>Plan Premium</h3>
			<p class="price">$150/mes</p>
			<p>Incluye beneficios adicionales y acumulación de puntos para el INFONAVIT</p>
			<button>Seleccionar</button>
		</div>
		<div class="plan">
			<h3>Plan Premium</h3>
			<p class="price">$150/mes</p>
			<p>Incluye beneficios adicionales y acumulación de puntos para el INFONAVIT</p>
			<button>Seleccionar</button>
		</div>
	</div>
</section>

<style>
	.pricing {
		padding: 4rem 2rem;
		text-align: center;
		background: #f5f5f5;
		font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
		color: #333;
	}

	.pricing h2 {
		font-size: 2.5rem;
		margin-bottom: 3rem;
		font-weight: 300;
		color: #222;
	}

	.plan-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 2rem;
	}

	.plan {
		background-color: white;
		padding: 3rem;
		border-radius: 10px;
		box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
		flex: 1 1 calc(33.333% - 2rem);
		max-width: calc(33.333% - 2rem);
		transition: transform 0.3s ease, box-shadow 0.3s ease;
	}

	.plan:hover {
		transform: translateY(-10px);
		box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
	}

	.plan h3 {
		font-size: 2rem;
		margin-bottom: 1rem;
		color: #111;
		font-weight: 400;
	}

	.plan .price {
		font-size: 1.5rem;
		margin-bottom: 1.5rem;
		color: #ff4081;
		font-weight: 700;
	}

	.plan p {
		font-size: 1rem;
		margin-bottom: 1.5rem;
		color: #555;
	}

	.plan button {
		background-color: #ff4081;
		color: white;
		border: none;
		padding: 1rem 2rem;
		font-size: 1rem;
		border-radius: 5px;
		cursor: pointer;
		transition: background-color 0.3s ease, box-shadow 0.3s ease;
	}

	.plan button:hover {
		background-color: #e00070;
		box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
	}

	@media (max-width: 1024px) {
		.plan {
			flex: 1 1 calc(30% - 2rem);
			max-width: calc(30% - 2rem);
		}
	}

	@media (max-width: 768px) {
		.plan {
			flex: 1 1 100%;
			max-width: 100%;
		}
	}
</style>
