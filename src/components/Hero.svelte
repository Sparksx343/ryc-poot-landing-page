<script>
	function hideScrollIndicator() {
		const indicator = document.querySelector('.scroll-indicator');
		if (indicator) {
			// @ts-ignore
			indicator.style.display = 'none';
		}
	}
	if (typeof window !== 'undefined') {
		window.addEventListener('scroll', hideScrollIndicator);
	}
</script>
<section class="hero">
	<div class="overlay"></div>
	<div class="content">
		<h1>Inscríbete al IMSS Fácil y Rápido</h1>
		<p>
			En Toop, nos especializamos en hacer que el proceso de afiliación al IMSS sea fácil, rápido y sin complicaciones.
		</p>
		<a href="tel:9613731566">
			<button>Programa una cita</button></a
		>
		
	</div>
</section>
<div class="scroll-indicator">
	<!-- svelte-ignore a11y-click-events-have-key-events -->
	<!-- svelte-ignore a11y-no-static-element-interactions -->
	<i class="fas fa-chevron-down"></i>
</div>

<style>
	.hero {
		background: url('../assets/fam.webp')
			no-repeat center center/cover;
		color: white;
		padding: 4rem 2rem;
		text-align: center;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		min-height: 80vh;
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
		top: 110px;
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
	.scroll-indicator {
		position: fixed;
		bottom: 1rem;
		left: 50%;
		transform: translateX(-50%);
		font-size: 2rem;
		color: white;
		animation: bounce 1.5s infinite;
		z-index: 100;
		cursor: pointer;
	}
	@keyframes bounce {
		0%,
		20%,
		50%,
		80%,
		100% {
			transform: translateY(0);
		}
		40% {
			transform: translateY(-10px);
		}
		60% {
			transform: translateY(-5px);
		}
	}
</style>