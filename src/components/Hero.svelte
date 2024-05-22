<!-- src/HeroSection.svelte -->
<script>
</script>

<section class="hero">
	<div class="overlay"></div>
	<div class="content">
		<h1>Inscríbete al IMSS Fácil y Rápido</h1>
		<p>
			Ofrecemos un servicio ágil para el registro al IMSS por una cuota mensual. Protege a tus
			familiares y asegúrate un futuro seguro con nuestras prestaciones.
		</p>
		<button>Regístrate Ahora</button>
	</div>
</section>

<style>
	.hero {
		background: url('https://www.metlifemas.com.mx/content/dam/metlifecom/mxmas/img/home/home_metlife_mas.jpg')
			no-repeat center center/cover;
		color: white;
		padding: 4rem 2rem;
		text-align: center;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		min-height: 70vh;
		position: relative;
	}

	.overlay {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: rgba(0, 0, 0, 0.5);
	}

	.content {
		position: relative;
		z-index: 1;
	}

	.hero h1 {
		font-size: 2.5rem;
		margin-bottom: 1rem;
	}

	.hero p {
		font-size: 1.2rem;
		margin-bottom: 2rem;
		max-width: 600px;
	}

	.hero button {
		background-color: #ff4081;
		color: white;
		border: none;
		padding: 1rem 2rem;
		font-size: 1rem;
		border-radius: 5px;
		cursor: pointer;
		transition: background-color 0.3s ease;
	}

	.hero button:hover {
		background-color: #e00070;
	}
</style>
