<script>
    import { onMount } from 'svelte';
    import tweet1 from '$lib/assets/tweet1.jpg';
    import xlogo from '$lib/assets/Xlogo.png';

    let showXLogo = false;
    let showTweet = false;

    onMount(() => {
        
        setTimeout(() => {
            showXLogo = true;
        }, 12000);
    });

    const handleClickXLogo = () => {

        showTweet = true;
    };

    const handleHideImages = () => {
        showXLogo = false;
        showTweet = false;
    };


    // Add event listener to hide images on click anywhere on the screen
</script>

{#if showXLogo}
    <img 
        alt="x logo" 
        src={xlogo} 
        class="xlogo" 
        on:click={handleClickXLogo} 
    />
{/if}

{#if showTweet}
    <div class="tweet">
        <button on:click={handleHideImages}>X</button>
        <img src={tweet1} alt="crispi tweet"/>
    </div>
{/if}

<style>
    .xlogo {
        position: fixed;
        bottom: 10px;
        right: 10px;
        width: 50px;
        height: 50px;
        animation: bounce 1s ease infinite;
        cursor: pointer;
    }

    @keyframes bounce {
        0%, 20%, 50%, 80%, 100% {
            transform: translateY(0);
        }
        40% {
            transform: translateY(-30px);
        }
        60% {
            transform: translateY(-15px);
        }
    }

    .tweet {
        position: fixed;
        bottom: 70px;
        right: 20px;
        background-color: white;
        padding: 10px;
        border-radius: 10px;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
        max-width: 30vw;
        height: auto;
    }

    img {
        max-width: 100%;
    }
</style>
