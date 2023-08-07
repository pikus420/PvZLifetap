<script>
	import Life from './Life.svelte';
	import Shields from './Shields.svelte';
	import BlockMeter from './BlockMeter.svelte';
</script>

<main>
	<div class="plants">
		<Life />
		<BlockMeter />
		<Shields />
	</div>
	<div class="zombies">
		<Life />
		<BlockMeter />
		<Shields />
	</div>

</main>

<style>
	.plants, .zombies{
		width: 100vw;
		height: 50vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.plants{
		background-color: #81ff81;
	}

	.zombies{
		background-color: #804ab3;
		transform: rotate(180deg);
	}
</style>