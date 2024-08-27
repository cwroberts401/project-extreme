<script>
    import image1 from '$lib/assets/ch3-main.gif';

    let answerSelected = false;
    let selectedAnswer = null;

    const handleClick = (ans) => {
        answerSelected = true;
        selectedAnswer = ans;
    }
</script>

<img alt="politician giving speech" src={image1}>
<div class="caption">
    <p class="name">Nicholas Mucci</p>
    <p>“White lives matter too”</p>
</div>

{#if !answerSelected}
    <div class="buttons">
        <button class="agree" on:click={() => handleClick("agree")}>AGREE</button>
        <button class="disagree" on:click={() => handleClick("disagree")}>DISAGREE</button>
    </div>
{:else}
    {#if selectedAnswer === "agree"}
        <div class="stats">
            <p>100% of other readers agree</p>
        </div>
    {:else}
        <div class="stats">
            <p>0% of other readers agree</p>
        </div>
    {/if}
{/if}


<style>
    img {
        max-width: 100%;
    }
    .caption {
        border-radius: 20px;
        width: 90%;
        height: max-content;
        background-color: white;
        margin: 0 auto;
        font-family: 'Courier New', Courier, monospace;
        padding: 10px 30px;
    }

    .stats {
        font-size: 20px;
        font-family: 'Courier New', Courier, monospace;
        color: white;
        text-align: center;
        margin-top: 20px;
    }

    .name {
        margin: 0;
        font-size: 20px;
        font-weight: 600;
    }

    p {
        margin: 0;
        
    }

    .agree {
        background-color: green;
    }

    .disagree{
        background-color: red;
    }

    button {
        border-radius: 10px;
        height: 40px;
        width: 150px;
        border: none;
        color: white;
    }

    .buttons {
        display: flex;
        justify-content: center;
        gap: 20px;
        margin-top: 20px;
    }
</style>
