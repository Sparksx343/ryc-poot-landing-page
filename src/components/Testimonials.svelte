<!-- src/TestimonialsSection.svelte -->
<script>
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';

	let testimonials = [
		{
        text: 'El servicio fue increíblemente rápido y sencillo. ¡Ahora mi familia y yo estamos asegurados!',
        author: 'Gabriel Torres'
    },
    {
        text: 'Me ayudaron a inscribirme al IMSS sin complicaciones. ¡Totalmente recomendado!',
        author: 'Laura Sánchez'
    },
    {
        text: 'Excelente atención y servicio. Estoy muy satisfecho.',
        author: 'Daniela Muñoz'
    },
    {
        text: 'Gracias a este servicio, pude inscribirme al IMSS fácilmente. ¡Muy agradecido!',
        author: 'Ricardo Flores'
    },
    {
        text: 'Servicio eficiente y rápido. Ahora estoy tranquilo sabiendo que estoy cubierto.',
        author: 'Sandra Velázquez'
    },
    {
        text: 'La atención al cliente fue excepcional, resolvieron todas mis dudas rápidamente.',
        author: 'Fernando Medina'
    },
    {
        text: 'Un servicio confiable y profesional. Me ayudaron con todo el proceso de inscripción.',
        author: 'Carmen Ortega'
    },
    {
        text: 'Gracias a este servicio, pude inscribirme al IMSS sin problemas. ¡Muy recomendable!',
        author: 'Alberto Núñez'
    },
    {
        text: 'El proceso de inscripción fue rápido y sin complicaciones. Excelente servicio.',
        author: 'Paola Rojas'
    },
	];

	function shuffle(array) {
		for (let i = array.length - 1; i > 0; i--) {
			const j = Math.floor(Math.random() * (i + 1));
			[array[i], array[j]] = [array[j], array[i]];
		}
		return array;
	}

	let displayedTestimonials = Array(3).fill().map(() => testimonials[Math.floor(Math.random() * testimonials.length)]);

	function updateTestimonial(index) {
		displayedTestimonials[index] = testimonials[Math.floor(Math.random() * testimonials.length)];
	}

	function getRandomInterval() {
		return Math.floor(Math.random() * (7000 - 3000 + 1)) + 3000;
	}

	onMount(() => {
		const intervals = displayedTestimonials.map((_, index) => setInterval(() => updateTestimonial(index), getRandomInterval()));
		return () => intervals.forEach(clearInterval);
	});
</script>

<section class="testimonials">
	<h2>Testimonios</h2>
	<div class="testimonial-row">
		{#each displayedTestimonials as { text, author }, index}
			<div class="testimonial" id={`testimonial-${index}`} transition:fade={{ duration: 500 }}>
				<p>"{text}"</p>
				<p>- {author}</p>
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
		height: 90px;
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
