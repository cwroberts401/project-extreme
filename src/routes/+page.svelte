<script>
    import Title from "../components/title.svelte";
    import Byline from "../components/byline.svelte";
    import Section1 from "../components/section1.svelte";
    import Section2 from "../components/section2.svelte";
    import Section3 from "../components/section3.svelte";
    import Section4 from "../components/section4.svelte";
    import Section5 from "../components/section5.svelte";
    import Credits from "../components/credits.svelte";
    import Messages from "../components/messages.svelte";
    import Chart from "../components/chart.svelte";
    import Threed from "../components/threed.svelte";
    import Interactive1 from "../components/interactive1.svelte";
</script>

<Title/>
<Byline/>

    <div>  
        <Section1/>
        <Interactive1/>
        <Section2/>
        <Section3/>
        <Section4/>
        <Section5/>
        <Credits/>
        <Messages/>
    </div>

<style>
    .container{
        display: flex;
    }
    
    .text{
        width: 70%;
    }
    .graph{
        width: 30%;
        background-color: white;
    }
</style>

