<script>
    let enabled = true;
    function changeShield(){
        if(enabled){
            enabled = false;
            navigator.vibrate(200);
        }
        else{
            enabled = true;
            navigator.vibrate(200);
        }
            
    }
	
</script>

<img src="../img/shield.png" alt="shield" class:removed={enabled === false} on:click={changeShield} on:keydown>

<style>
    img{
        height: 55px;
        width: 50px;
        transition: linear 0.3s;
    }

    .removed{
        opacity: 0.5;
    }
</style>