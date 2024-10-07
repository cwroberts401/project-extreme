<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Michroma&display=swap" rel="stylesheet">
</svelte:head>

<script>
import imm1 from '$lib/assets/flag-blu.png';
import imm2 from '$lib/assets/project extreme logo.png';
</script>

<div class="logo-bg">
    <img alt="Project Extreme logo" src={imm2}/>
</div>
<div class="title-bg">
    <div style="grid-row: 1/2" class="title-line"><h2>INSIDE THE</h2><div class="white-bar"></div></div>
    <div style="grid-row: 2/3" class="title-line"><h2 style="color:#bd1e2d">MAINSTREAMING</h2><div class="red-bar"></div></div>
    <div style="grid-row: 3/4" class="title-line"><h2>OF HATE.</h2><div class="white-bar"></div></div>
    <div style="grid-row: 4/5" class="title-line"><h2 style="color:#bd1e2d">HOW TOXIC</h2><div class="red-bar"></div></div>
    <div style="grid-row: 5/6" class="title-line"><h2>INFLUENCERS</h2><div class="white-bar"></div></div>
    <div style="grid-row: 6/7" class="title-line"><h2 style="color:#bd1e2d">ARE PUSHING</h2><div class="red-bar"></div></div>
    <div style="grid-row: 7/8" class="title-line"><h2>N.J. POLITICS</h2><div class="white-bar"></div></div>
    <div style="grid-row: 8/9" class="title-line"><h2 style="color:#bd1e2d">TO THE</h2><div class="red-bar"></div></div>
    <div style="grid-row: 9/10" class="title-line"><h2>FAR RIGHT</h2><div class="white-bar"></div></div>
    <div class="spacer"></div>
    <div class="title-image">
    <img style="grid-row: 6/10" alt="faces of Soloway, Crispi, and Durr on a blue background" src={imm1}/>
    </div>
</div>

<style>
    .title-bg {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr; /* 2 columns */
        grid-template-rows: 50px 50px 50px 50px 50px 50px 50px 50px 50px; /* 9 rows with explicit height */
        /* 9 rows */
        gap: 10px; /* Optional: space between items */
    }

    .title-line {
        grid-column: 1 / -1; /* Span both columns */
    }

    .title-image {
        grid-column: 4/6; /* Place in the right column */
        grid-row: 6 / span 4;
        margin: 10px 1vw 0 0;
    }

    .spacer{
        grid-row: 1 / span 5;
        grid-column: 4/6;
        margin: 10px 10px 0 0;
    }

    .title-image>img{
        width: 100%;
        height: 230px;
        display: block;
    }

    .logo-bg{
        width: 100%;
        display: flex;
    }

    .logo-bg>img{
        width: 200px;
        margin: 20px auto;
    }
    .title-line{
        max-width: 98vw;
        width: 98vw;
        display: flex;
        margin: 10px 1vw 0 1vw;
    }
    .title-line > h2 {
        width: max-content;
        white-space: nowrap;
        color: white;
        font-family: "Bebas Neue", sans-serif;
        font-size: 60px;
        margin: 0;
        line-height: 50px;
    }
    .white-bar{
        margin: 0 0 0 10px;
        width: 100%;
        height: 50px;
        background-color: white;
    }
    .red-bar{
        margin: 0 0 0 10px;
        width: 100%;
        height: 50px;
        background-color: #bd1e2d;
    }

    @media (max-width: 768px) {
        .title-bg {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
        grid-template-rows: 30px 30px 30px 30px 30px 30px 30px 30px 30px;
        gap: 5px;
        }

        .title-image>img{
        width: 100%;
        height: 135px;
        display: block;
    }

        .title-line > h2 {
        width: max-content;
        white-space: nowrap;
        color: white;
        font-family: "Bebas Neue", sans-serif;
        font-size: 40px;
        margin: 2px 0 0 0;
        line-height: 30px;
    }
        .white-bar{
            height: 30px;
        }
        .red-bar{
            height: 30px;
        }

        .txt-half>img {
        max-width: 100%;
        height: 72px;
        margin: 50px 1vw 0px 0;
        float: right;
        transform: translateY(85px);
        }

        .mob{
            display: block;
        }
    }
</style>