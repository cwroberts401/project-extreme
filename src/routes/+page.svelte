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
    import Interactive3 from "../components/interactive3.svelte";
    import Interactive2 from "../components/interactive2.svelte";
    import InfoModal from "../components/info-modal.svelte";
    import Img4 from "../components/img4.svelte";
    import Img5 from "../components/img5.svelte";
</script>

<Title/>
<Byline/>

    <div>  
        <InfoModal/>
        <Section1/>
        <Chart/>

        <!--<Interactive2/>-->
        <Interactive1/>
        <Section2/>
        <Interactive3/>
        <Section3/>
        <Img4/>
        <Section4/>
        <Img5/>
        <Section5/>
        <Credits/>
    </div>

<style>

</style>

