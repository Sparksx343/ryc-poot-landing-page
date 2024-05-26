<script>
	import { Parallax, ParallaxLayer } from 'svelte-parallax';

	let parallax;
	let disabled = false;
	let fancy = 'Bonito'.split('');
</script>

<!-- <button class="disable" on:click={() => disabled = !disabled}>disable</button> -->
<div class="body">

	<Parallax sections={3} bind:this={parallax} {disabled}>
		{#each fancy as char, index (index)}
		<ParallaxLayer
		rate={(index + 1) / (fancy.length - 1)}
		offset={1}
		style="
		margin-left: {38 + index * 5}%; 
		display: flex; 
		justify-content: flex-start; 
		align-items: center;
		"
		>
		<p class="fancy">
			{char}
		</p>
	</ParallaxLayer>
	{/each}
	
	<ParallaxLayer offset={1} rate={-2.5} style="display: flex; justify-content: flex-end;">
		<div style="background-color: lightblue; opacity: 0.5; width: 50%; height: 100%;" />
	</ParallaxLayer>
	
	<ParallaxLayer offset={1} rate={2.5} style="display: flex; justify-content: flex-start;">
		<div style="background-color: yellow; opacity: 0.5; width: 50%; height: 100%;" />
	</ParallaxLayer>
	
	<ParallaxLayer
	rate="1"
	style="
	background-color: pink; 
	display: flex; 
	justify-content: center; 
	align-items: center; 
	flex-direction: column;
	"
	>
	<h1>scrollea!</h1>
	<!-- <button 
		class="bottom-btn" 
		on:click={() => parallax.scrollTo(3, {selector: '.top-btn', duration: 4000})}
		>
		Click me!
	</button> -->
</ParallaxLayer>

<ParallaxLayer
offset="2"
rate="2"
style="
background-color: pink; 
display: flex; 
justify-content: center; 
align-items: center;
"
></ParallaxLayer>
</Parallax>
</div>
<style>
	.body{
		background-color: rgb(11, 219, 140);
	}
	h1 {
		font-size: 2rem;
	}
	.fancy {
		font-size: 2.5rem;
	}
</style>
