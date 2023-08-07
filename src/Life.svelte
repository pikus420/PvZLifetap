<script>
    import LifeButton from './LifeButton.svelte';
    export let life = 20;

    function healing(){
        life++;
    }

    function damaging(){
        life--;
    }
</script>


<div class="life_container">
    <LifeButton type="+" on:click={healing}/>
    <p class="life">{life}</p>
    <LifeButton type="-" on:click={damaging}/>
</div>


<style>
    .life_container{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    p {
		font-size: 42px;
		font-weight: 500;
        user-select: none;
        margin: 0;
	}

    
</style>