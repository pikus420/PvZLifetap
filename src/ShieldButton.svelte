<script>
    let enabled = true;
    function changeShield(){
        if(enabled)
            enabled = false;
        else
            enabled = true;
    }
	
</script>

<img src="../img/shield.png" alt="shield" class:removed={enabled === false} on:click={changeShield} on:keydown>

<style>
    img{
        height: 35px;
        width: 30px;
    }

    .removed{
        opacity: 0.5;
    }
</style>