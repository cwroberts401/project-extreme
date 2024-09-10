<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Michroma&display=swap" rel="stylesheet">
</svelte:head>

<script>
    import imm1 from '$lib/assets/flag revised.gif';
    import imm2 from '$lib/assets/extreme-logo.png';
</script>

<!--
<div class="title-bg">
    <div class="title-line"><h2>INSIDE THE</h2><div class="white-bar"></div></div>
    <div class="title-line"><h2 style="color:red">MAINSTREAMING OF HATE.</h2><div class="red-bar"></div></div>
    <div class="title-line"><h2>HOW TOXIC</h2><div class="white-bar"></div></div>
    <div class="half">
        <div class="txt-half">
            <div class="title-line"><h2 style="color:red">INFULENCERS ARE</h2><div class="red-bar"></div></div>
            <div class="title-line"><h2>PUSHING N.J. POLITICS</h2><div class="white-bar"></div></div>
            <div class="title-line"><h2 style="color:red">TO THE FAR RIGHT</h2><div class="red-bar"></div></div>
        </div>
        <div class="txt-half">
            <img alt="faces" src={imm1}/>
        </div>
    </div>
    
</div> -->
<div class="wrapper">
    <img class="icon" src={imm2} alt="Project Extreme Part 1"/>
</div>
<div class="container">
    <img alt="faces" src={imm1}/>
</div>

<style>
    .container {
        display: flex;
        justify-items: center;
    }

    .wrapper {
        margin-top: 5px;
        width: 100%;
        display: flex;
        justify-content: center;
    }

    .icon{
        max-width: 180px;
        height: auto;
    }

.title-line{
        max-width: 90vw;
        width: 90vw;
        display: flex;
        margin: 20px 5vw 0 5vw;
    }

    .txt-half{
        width: 50%;
        max-width: 50%;
    }
    .half {
        display: flex;
    }

    img {
        width: 1000px;
        max-width: 100%;
        margin: 10px auto;
    }

    .title-line > h2 {
        width: max-content;
        white-space: nowrap;
        color: white;
        font-family: "Bebas Neue", sans-serif;
        font-size: 50px;
        margin: 2px 0 0 0;
        line-height: 40px;
    }

    h1 {
        color: white;
        text-align: center;
        font-family: 'Courier New', Courier, monospace;
        font-size: 15px;
        font-weight: 400;
        margin-top: -10px;
    }

    .white-bar{
        margin: 0 0 0 10px;
        width: 90%;
        height: 40px;
        background-color: white;
    }

    .red-bar{
        margin: 0 0 0 20px;
        width: 90%;
        height: 40px;
        background-color: red;
    }
</style>