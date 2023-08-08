<script>
	import Life from './Life.svelte';
	import Shields from './Shields.svelte';
	import BlockMeter from './BlockMeter.svelte';
	import Mana from './Mana.svelte';
</script>

<main>
	<div class="plants">
		<div class="counters">
			<Life />
			<Mana type="sun"/>
		</div>
		<BlockMeter />
		<Shields />
	</div>
	<div class="zombies">
		<div class="counters">
			<Life />
			<Mana type="brain"/>
		</div>
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
		transform: rotate(180deg);
	}

	.zombies{
		background-color: #804ab3;
	}

	.counters{
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		gap: 50px;
	}


	@media only screen and (min-width: 600px) {
		.plants, .zombies{
			width: 50%;
			height: 100vh;
		}
		main{
			display: flex;
		}
	}
</style>