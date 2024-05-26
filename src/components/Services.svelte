<script>
	import actas from '../assets/services/actas.webp';
	import imss from '../assets/services/imss.webp';
	import infonavit from '../assets/services/infonavit.webp';
	import curp from '../assets/services/curp.webp';
	import cfe from '../assets/services/cfe.webp';
	import marketing from '../assets/services/marketing.webp';
	import email from '../assets/services/email.webp';
	import issste from '../assets/services/issste.webp';
	import sat from '../assets/services/sat.webp';
	import ine from '../assets/services/ine.webp';
	import visa from '../assets/services/visa.webp';

	const services = [
		{
			title: 'Actas',
			description: ['Nacimiento', 'Defunción', 'Matrimonio', 'Divorcio'],
			img: actas,
			imgTitle: 'Actas'
		},
		{
			title: 'IMSS',
			description: ['Vigencia de derechos', 'Semanas cotizadas', 'Número de seguro social'],
			img: imss,
			imgTitle: 'IMSS'
		},
		{
			title: 'INFONAVIT',
			description: [
				'Aviso de retención',
				'Aviso de suspensión',
				'Estado de mi cuenta',
				'Reseteo de cuenta',
				'Creación de cuenta',
				'Taller saber para decidir'
			],
			img: infonavit,
			imgTitle: 'INFONAVIT'
		},
		{
			title: 'CFE',
			description: ['Pago de recibo de luz'],
			img: cfe,
			imgTitle: 'CFE'
		},
		{
			title: 'CURP',
			description: ['Descarga de CURP'],
			img: curp,
			imgTitle: 'CURP'
		},
		{
			title: 'Marketing',
			description: ['Diseño de tarjeta digitales de servicios'],
			img: marketing,
			imgTitle: 'Marketing'
		},
		{
			title: 'Correo Electrónico',
			description: ['Creación de correos electrónicos'],
			img: email,
			imgTitle: 'email'
		},
		{
			title: 'ISSSTE',
			description: [
				'Constancia de no afiliación',
				'Constancia de no derechohabiencia',
				'Descarga de comprobantes de pago a pensionistas',
				'Acreditación de la vigencia de derechos'
			],
			img: issste,
			imgTitle: 'ISSSTE'
		},
		{
			title: 'SAT',
			description: ['Citas SAT', 'Constancia de situación fiscal', 'Renocavión de contraseña CIEC'],
			img: sat,
			imgTitle: 'SAT'
		},
		{
			title: 'INE',
			description: ['Citas INE'],
			img: ine,
			imgTitle: 'SAT'
		},
		{
			title: 'VISA',
			description: ['Citas VISA'],
			img: visa,
			imgTitle: 'VISA'
		}
	];
</script>

<div class="grid-container">
	{#each services as service}
	<div class="card">
			<a href={`https://wa.me/529613731566?text=Hola%20estoy%20interesado%20en%20su%20sercicio%20de%20${service.title}`} class="whatsapp-button" target="_blank">
				<img src={service.img} alt={service.imgTitle} />
				<div class="card-content">
					<h2>{service.title}</h2>
					<ul>
						{#each service.description as description}
						<a href={`https://wa.me/529613731566?text=Hola%20estoy%20interesado%20en%20su%20sercicio%20de%20${description.toLocaleUpperCase()}%20del%20${service.title}`} class="whatsapp-button" target="_blank">
							<li>{description}</li>
						</a>
							{/each}
					</ul>
				</div>
			</a>
		</div>
	{/each}
</div>

<style>
	a,
	a:hover,
	a:focus,
	a:active {
		text-decoration: none;
		color: inherit;
	}
	.grid-container {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
		gap: 20px;
		padding: 20px;
	}

	.card {
		background-color: #fff;
		border-radius: 10px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
		overflow: hidden;
		transition:
			transform 0.7s ease,
			box-shadow 0.7s ease;
	}

	.card:hover {
		transform: translateY(-10px);
		box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
	}

	.card img {
		width: 100%;
		height: 200px;
		object-fit: cover;
		transition: transform 0.7s ease;
	}

	.card:hover img {
		transform: scale(1.1);
	}

	.card-content {
		padding: 20px;
		transition: background-color 0.3s ease;
	}

	.card:hover .card-content {
		background-color: #f0f0f0;
	}

	.card-content h2 {
		font-size: 1.5rem;
		margin-top: 0;
		margin-bottom: 10px;
		transition: color 0.3s ease;
	}

	.card:hover .card-content h2 {
		color: #007bff;
	}

	.card-content ul {
		list-style-type: none;
		padding-left: 0;
	}

	.card-content li {
		font-size: 1rem;
		color: #555;
		margin-top: 5px;
	}

	.card-content li::before {
		content: '•';
		color: #007bff;
		display: inline-block;
		width: 1em;
		margin-left: -1em;
	}
	li:hover{
		color: #007bff;
	}
</style>
