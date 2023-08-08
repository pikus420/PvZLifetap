<script>
    import ManaButton from './NumberButton.svelte';
    export let mana = 1;
    export let type;

    function addMana(){
        navigator.vibrate(200);
        mana++;
    }

    function substractMana(){
        navigator.vibrate(200);
        mana--;
    }
</script>


<div class="mana_container">
    <ManaButton type="+" on:click={addMana}/>
    <div class="number">
        <img src="/img/{type}.png" alt="{type}">
        <p class="mana">{mana}</p>
    </div>
    <ManaButton type="-" on:click={substractMana}/>
</div>


<style>
    .mana_container{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    .number{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: row;
        gap: 10px;
    }

    p {
		font-size: 42px;
        user-select: none;
        font-weight: 600;
        margin: 0;
	}

    img{
        width: 35px;
        height: 35px;
    }

    
</style>