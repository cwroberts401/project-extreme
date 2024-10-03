
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
    <div class="title-line"><div style="margin: 0;" class="white-bar"></div></div>
    <div class="title-line"><div style="margin: 0;" class="red-bar"></div></div>
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
            <img alt="faces of Soloway, Crispi, and Durr on a blue background" src={imm1}/>
        </div>
    </div>
    <div class="mob title-line"><div style="margin: 0;" class="white-bar"></div></div>
    <div class="mob title-line"><div style="margin: 0;" class="red-bar"></div></div>
    
</div>

<style>

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
    .txt-half{
        width: 50%;
        max-width: 50%;
    }
    .half {
        display: flex;
    }
    .txt-half>img {
        max-width: 100%;
        height: 174px;
        margin: 10px 1vw 0px 0;
        float: right;
    }

    .mob{
        display: none;
    }
    .title-line > h2 {
        width: max-content;
        white-space: nowrap;
        color: white;
        font-family: "Bebas Neue", sans-serif;
        font-size: 60px;
        margin: 2px 0 0 0;
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
        background-color: red;
    }

    @media (max-width: 768px) {
        .title-bg {
            max-width: 100%;
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