<script>
    let charges = 0;

    function addSections(){
        let sections = Math.floor(Math.random() * 3) + 1;
        charges += sections;

        if(charges >= 8){
            charges = 0;
            navigator.vibrate(400);
        }
        else{
            navigator.vibrate(200);
        }
            
    }
</script>

<div class="meter" on:click={addSections} on:keydown>
    <div class="sections" class:one={charges === 1} class:two={charges === 2} class:three={charges === 3} class:four={charges === 4} class:five={charges === 5} class:six={charges === 6} class:seven={charges === 7} class:eight={charges === 8}></div>
    <div class="lines line1"></div>
    <div class="lines line2"></div>
    <div class="lines line3"></div>
    <div class="lines line4"></div>
    <div class="lines line5"></div>
    <div class="lines line6"></div>
    <div class="lines line7"></div>
</div>

<style>
    .meter{
        width: 240px;
        height: 30px;
        background-color: #b7b7b7;
        border: 2px solid #000;
    }
    .sections{
        width: 0px;
        height: 30px;
        background-color: #2a9fff;
    }

    .lines{
        position: relative;
        z-index: 3;
        background-color: #000;
        height: 30px;
        width: 1px;
    }

    .line1{
        left: 30px;
        top: -30px;
    }

    .line2{
        left: 60px;
        top: -60px;
    }

    .line3{
        left: 90px;
        top: -90px;
    }

    .line4{
        left: 120px;
        top: -120px;
    }

    .line5{
        left: 150px;
        top: -150px;
    }

    .line6{
        left: 180px;
        top: -180px;
    }

    .line7{
        left: 210px;
        top: -210px;
    }

    .one{
        width: 30px;
    }

    .two{
        width: 60px;
    }

    .three{
        width: 90px;
    }

   .four{
        width: 120px;
   }

   .five{
        width: 150px;
   }

   .six{
        width: 180px;
   }

   .seven{
        width: 210px;
   }

    .eight{
        width: 240px;
    }

</style>