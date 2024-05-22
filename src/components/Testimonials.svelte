<!-- src/TestimonialsSection.svelte -->
<script>
	let testimonials = [
		{
			text: 'El servicio me facilitó el proceso de inscripción al IMSS y ahora mi familia está protegida. ¡Recomendado!',
			author: 'Juan Pérez'
		},
		{
			text: 'Rápido y eficiente, ahora tengo tranquilidad sabiendo que estoy cubierto ante cualquier eventualidad.',
			author: 'María López'
		},
		{
			text: 'El servicio me facilitó el proceso de inscripción al IMSS y ahora mi familia está protegida. ¡Recomendado!',
			author: 'Juan Pérez'
		}
	];
</script>

<section class="testimonials">
	<h2>Testimonios</h2>
	<div class="testimonial-row">
		{#each testimonials as { text, author }, index}
			<div class="testimonial" id={`testimonial-${index}`}>
				<p>{text}</p>
				<p>{author}</p>
			</div>
		{/each}
	</div>
</section>

<style>
	.testimonials {
		background-color: #fff;
		padding: 4rem 2rem;
		text-align: center;
	}

	.testimonials h2 {
		font-size: 2rem;
		margin-bottom: 2rem;
	}

	.testimonial-row {
		display: grid;
		grid-template-columns: repeat(3, minmax(200px, 1fr));
		gap: 2rem;
	}

	.testimonial {
		background: #f9f9f9;
		padding: 1rem;
		border-radius: 8px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
	}

	.testimonial p:first-of-type {
		font-style: italic;
		margin-bottom: 1rem;
	}

	.testimonial p:last-of-type {
		font-weight: bold;
	}

	@media (max-width: 768px) {
		.testimonial-row {
			grid-template-columns: 1fr;
		}
	}
</style>
