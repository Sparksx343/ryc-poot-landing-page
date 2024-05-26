<script>
	import easy from '../assets/easy.webp';
	import fast from '../assets/fast.webp';
	import support from '../assets/support.webp';
	import realtimenotify from '../assets/realtimenotify.webp';
</script>

<section class="features">
	<h2>¿Por qué elegirnos?</h2>
	<div class="feature-row">
		<div class="feature">
			<img src={easy} alt="Feature 1" />
			<h3>Proceso Simplificado</h3>
			<p>
				Nuestro sistema intuitivo te guía paso a paso, eliminando la confusión y los errores
				comunes. Con instrucciones claras y directas, te aseguramos que completarás tu afiliación
				sin complicaciones.
			</p>
		</div>
		<div class="feature">
			<img src={fast} alt="Feature 2" />
			<h3>Ahorro de Tiempo</h3>
			<p>
				Sabemos que tu tiempo es valioso. Por eso, nuestro servicio está diseñado para que realices
				tu afiliación en cuestión de minutos, evitando largas esperas y trámites innecesarios.
			</p>
		</div>
		<div class="feature">
			<img src={support} alt="Feature 3" />
			<h3>Soporte Profesional</h3>
			<p>
				No estás solo. Nuestro equipo de expertos está siempre disponible para asistirte en cada
				etapa del proceso. Ya sea a través de chat en vivo, correo electrónico o teléfono, estamos
				aquí para resolver tus dudas y asegurarnos de que tu experiencia sea fluida.
			</p>
		</div>
		<div class="feature">
			<img src={realtimenotify} alt="Feature 3" />
			<h3>Actualizaciones en Tiempo Real</h3>
			<p>
				Mantente informado en cada paso del proceso. Recibirás notificaciones en tiempo real sobre
				el estado de tu solicitud, desde la recepción de documentos hasta la confirmación final de
				tu afiliación.
			</p>
		</div>
	</div>
</section>

<style>
	:root {
		--primary-color: #2c3e50;
		--secondary-color: #2c3e50;
		--bg-color: #ecf0f1;
		--text-color: #2c3e50;
		--border-radius: 10px;
		--box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
	}

	.features {
		padding: 4rem 2rem;
		background-color: var(--bg-color);
		text-align: center;
	}

	.features h2 {
		font-size: 2.5rem;
		color: var(--primary-color);
		margin-bottom: 3rem;
	}

	.feature-row {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 2rem;
	}

	.feature {
		flex: 1 1 calc(20% - 2rem);
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		padding: 2rem;
		background: white;
		border-radius: var(--border-radius);
		box-shadow: var(--box-shadow);
		transition: transform 0.3s ease, box-shadow 0.3s ease;
	}

	.feature:hover {
		transform: translateY(-10px);
		box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
	}

	.feature img {
		max-width: 100%;
		height: auto;
		margin-bottom: 1.5rem;
		border-radius: var(--border-radius);
	}

	.feature h3 {
		font-size: 1.75rem;
		color: var(--secondary-color);
		margin-bottom: 1rem;
	}

	.feature p {
		font-size: 1rem;
		color: var(--text-color);
		line-height: 1.6;
	}

	@media (max-width: 768px) {
		.feature {
			flex: 1 1 100%;
		}
	}
</style>
