<script>
// ##001 : declare and initialize 2 variables dice and rolls
    let dice = 0;
    let rolls = [];
// ##002 : declare and define the reactive var total
    $: total = rolls.reduce((t, n) => t + n, 0)
// ##003 : declare the roll function
    function roll() {
        dice = Math.floor(Math.random() * Math.floor(5)) + 1
// ##004 : instead of using push() method, we are using destructuring and assignement
        rolls = [...rolls, dice]
    }
// ##005 : restart() function
    function restart() {
        dice = 0
        rolls = []
    }
</script>

<h1>Number is: {dice}</h1>
<div>Number of rolls: {rolls.length}</div>
<div>Total: {total}</div>
<button on:click={roll}>Let's roll the dice</button>
<button on:click={restart}>Restart</button>

<p>
    { rolls.toString() }
</p>
<div>
    {#each rolls as t, index}
        {#if index == rolls.length -1}
            <b style="background-color: lightgreen;">{t}</b>
        {:else}
            {t} -&nbsp;
        {/if}

    {/each}
</div>
