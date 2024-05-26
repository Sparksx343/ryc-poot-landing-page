<script>
	import logo from '../assets/logo.png';
	import { goto } from '$app/navigation';
	let menuOpen = false;

	function toggleMenu() {
		menuOpen = !menuOpen;
	}
	function goToHome(){
		goto('/')
	}
</script>

<header>
	<!-- svelte-ignore a11y-click-events-have-key-events -->
	<!-- svelte-ignore a11y-no-static-element-interactions -->
	<div class="logo" on:click={goToHome} >
		<img src={logo} alt="Logo" class="logo"/>
		<h1>Toop</h1>
	</div>
	<button class="menu-button" on:click={toggleMenu}>
		<i class="fas fa-bars"></i>
	</button>
	<nav class={menuOpen ? 'open' : ''}>
		<a href="tel:9613731566">
			<i class="fas fa-phone"></i>
			(961) - 3731 - 566</a
		>
		<a href="/">
			<i class="fas fa-home"></i>
			Inicio
		</a>
		<a href="/services">
			<i class="fas fa-concierge-bell"></i>
			Servicios
		</a>
		<a href="/about">
			<i class="fas fa-info-circle"></i>
			Acerca
		</a>
	</nav>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem 2rem;
		background: linear-gradient(90deg, #4b6cb7, #182848);
		color: white;
		box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
		position: relative;
	}
	.logo {
		display: flex;
		align-items: center;
		cursor: pointer;
	}
	.logo > img {
		height: 40px;
		margin-right: 20px;
	}
	.logo h1 {
		margin: 0;
		font-size: 1.8rem;
		font-weight: bold;
	}

	nav {
		display: flex;
		gap: 1rem;
		align-items: center;
		z-index: 2;
	}

	nav a {
		color: white;
		text-decoration: none;
		padding: 0.5rem 1rem;
		border-radius: 5px;
		transition:
			background-color 0.3s ease,
			transform 0.3s ease;
		display: flex;
		align-items: center;
		gap: 0.5rem;
	}

	nav a:hover {
		background-color: rgba(255, 255, 255, 0.2);
		transform: scale(1.1);
	}

	.menu-button {
		display: none;
		cursor: pointer;
		background: none;
		border: none;
		font-size: 1.8rem;
		color: white;
	}

	@media (max-width: 300px) {
		.logo > img {
			display: none;
		}
	}
	@media (max-width: 768px) {
		nav {
			display: none;
			flex-direction: column;
			gap: 0;
			width: 100%;
			position: absolute;
			top: 100%;
			left: 0;
			background: linear-gradient(90deg, #4b6cb7, #182848);
			box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
			transition:
				max-height 0.3s ease,
				opacity 0.3s ease;
			max-height: 0;
			overflow: hidden;
			opacity: 0;
		}

		.menu-button {
			display: block;
		}

		nav.open {
			display: flex;
			max-height: 300px;
			opacity: 1;
		}
	}

</style>
