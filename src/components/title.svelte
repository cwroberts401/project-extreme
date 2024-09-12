
<script>
    import imm1 from '$lib/assets/flag revised.gif';
    import imm2 from '$lib/assets/extreme-logo.png';
</script>

<div class="wrapper">
    <img class="icon" src={imm2} alt="Project Extreme Part 1"/>
</div>
<div class="container">
    <img alt="faces" src={imm1}/>
</div>

<style>
    .container {
        display: flex;
        justify-content: center;
        width: 100%;
        overflow: hidden;
    }

    .container img {
        width: 100%;
        max-width: 100vw;
        height: auto;
        object-fit: contain;
    }

    @media (min-width: 1000px) {
        .container img {
            max-width: 1000px;
        }
    }

    .wrapper {
        margin-top: 5px;
        width: 100%;
        display: flex;
        justify-content: center;
    }

    .icon {
        max-width: 180px;
        height: auto;
    }

    @media (min-width: 768px) {
        .icon {
            max-width: 220px;
        }
    }

    img {
        width: 1000px;
        max-width: 100%;
        margin: 10px auto;
    }

</style>