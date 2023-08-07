<script>
    let charges = 0;

    function addSections(){
        let sections = Math.floor(Math.random() * 3) + 1;
        charges += sections;

        if(charges >= 8)
            charges = 0;
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
        width: 200px;
        height: 25px;
        background-color: #b7b7b7;
        border: 2px solid #000;
    }
    .sections{
        width: 0px;
        height: 25px;
        background-color: #2a9fff;
    }

    .lines{
        position: relative;
        z-index: 3;
        background-color: #000;
        height: 25px;
        width: 1px;
    }

    .line1{
        left: 25px;
        top: -25px;
    }

    .line2{
        left: 50px;
        top: -50px;
    }

    .line3{
        left: 75px;
        top: -75px;
    }

    .line4{
        left: 100px;
        top: -100px;
    }

    .line5{
        left: 125px;
        top: -125px;
    }

    .line6{
        left: 150px;
        top: -150px;
    }

    .line7{
        left: 175px;
        top: -175px;
    }

    .one{
        width: 25px;
    }

    .two{
        width: 50px;
    }

    .three{
        width: 75px;
    }

   .four{
        width: 100px;
   }

   .five{
        width: 125px;
   }

   .six{
        width: 150px;
   }

   .seven{
        width: 175px;
   }

    .eight{
        width: 200px;
    }

</style>