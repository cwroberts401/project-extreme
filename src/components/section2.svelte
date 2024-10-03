<script>
    import '../styles/section-styles.css';
    import info1 from '$lib/assets/crispi-quote.png';
    import chIco from '$lib/assets/rino.png';
    import image1 from '$lib/assets/ch-2-chart.png';
    import TreeModal from './info-modal.svelte';
    import durr from '$lib/assets/durr.jpg';

</script>

<div class="section-container">
  <div class="section-title">
    <img class="ch-icon" src={chIco} alt="republician elephant"/>
    <h3> Chapter 2 </h3>
    <h4> A Web of Influencers </h4>
  </div>
    
    <div>
        <p>A large tent shaded the courtyard behind McDonagh’s Pub & Restaurant in Keyport.</p>
        <p>American flags flapped in the March wind next to Trump flags as more than 200 people descended on the Jersey Shore community for another “Hands Off My Ballot” rally.</p>
        <p>Congressional candidates and local officials mingled on the blacktop. Children chased each other as their parents sat at picnic tables. People with clipboards collected signatures. And merchandise tables sold Trump buttons, shirts and hats.</p>
        <img alt="quote" src={info1}/>
        <p>Crispi, wearing a white shirt and dark suit jacket, then stepped to the microphone.</p>
        <p>He stoked the crowd by telling them they were “second-class citizens in our own country.”</p>
        <p>“The illegal immigrants (are) coming in, and they’re not migrants, they’re illegals, coming into this country, savagely harming people,” said Crispi, who in 2022 ran unsuccessfully for Congress in the 4th District.</p>
        <p id="ingrassia">He would stand shoulder-to-shoulder with 
          <TreeModal 
      name={"Paul Ingrassia"}
      facts={["Substack writer", "Has attended events with Mike Crispi and Cynthia Hughes",]}
      treeTop={[{ name: "Mike Crispi", link: "#crispi" }]} 
      treeMid={[{ name: "Paul Ingrassia", link: null, main: true }, { name: "Cynthia Hughes", link: "#hughes", main: false }]} 
      treeBottom={[]}
    >
          <span class="highlight" title="Click to learn more about this character">Ingrassia</span> 
        </TreeModal>
        and other activists like Hughes in front of the audience.</p>
        <p>“This is about the weaponization of government on every level that you could possibly think of,” she told the crowd, referring to the prosecution of Jan. 6 rioters.</p>
        <p>Hughes did not respond to interview requests via email and a letter left at her home.</p>
        <p>As this event demonstrated, the far-right in New Jersey is a web, with Crispi often at its center. Here is an abridged version of their ties, six degrees of separation-style:</p>
        <p id="durr">Crispi has <a href="https://nyyrc.com/events/nj-invasion-and-liberation-event-with-mike-crispi-bill-spadea/">hosted events with Spadea</a>, who has endorsed <a href="https://mikecrispi.com/endorsements">Crispi</a>,  
          <TreeModal 
      name={"Ed Durr"}
      facts={["Known as Ed 'the Trucker' Durr", "Former Republican state senator", "Spoke at event in Shamong"]}
      treeTop={[{ name: "LINK HERE", link: null }]} 
      treeMid={[{ name: "Mike Crispi", link: null, main: true }, { name: "LINK HERE", link: null, main: false }]} 
      treeBottom={[]}
      imageUrl={durr}
    >
          <span class="highlight" title="Click to learn more about this character"> Durr </span>
        </TreeModal>
        and <a href="https://nj1015.com/raucous-crowd-in-clark-nj-ready-to-win/">Santos.</a></p>
        <p id="stouffer">Durr has been a featured speaker at events with Spadea, Santos and 
          <TreeModal 
      name={"Nicole Stouffer"}
      facts={["Founder of the New Jersey Project", "Co-hosted event in Shamong with America First Republicans of New Jersey", "Co-hosts event with Concerned Citizens of New Jersey"]}
      treeTop={[{ name: "the New Jersey Project", link: null }]} 
      treeMid={[{ name: "Paul Ingrassia", link: "#ingrassia", main: false }, { name: "Nicole Stouffer", link: null, main: true }, { name: "Mike Crispi", link: "#crispi", main: false }]} 
      treeBottom={[]}
    >
          <span class="highlight" title="Click to learn more about this character">Stouffer.</span>
          </TreeModal>
          </p>
        <p>Stouffer has aligned herself with Crispi and co-hosted the Shamong event with his America First group. Her organization has also co-hosted events with Mack. Santos promotes Mack’s website on his <a href="https://unioncountyvote.org/index.php">own site.</a></p>
        <p>Crispi is also aligned with Ingrassia, who endorsed Santos at a fundraiser in February.</p>
        <p>Everyone gathered in Keyport seemed to agree there’s a growing market for right-wing views in straight-talking New Jersey. In fact, these advocates believe they might even turn the state red this November for the first time in decades.</p>
        <img src={image1}/>
        <p>Even if every prognosticator still sees the state as solidly blue, these influencers are slowly recasting the state GOP by roiling conservative corners of New Jersey. They’re rallying voters on a grassroots level — especially in blue-collar communities in Northwest Jersey, along the Shore and throughout South Jersey – and pressuring establishment Republicans further right.</p>
        <p>“What we do here today,” Crispi said, “will change the course of history. Because New Jersey goes red — landslide, undeniable momentum — and that's how we're going to make America great again.”</p>
        <p>The crowd — dotted with local officials such as Araneo, Alexandria Township Committeeman Tom Hudanish and Francisco, the former executive director of <a href="https://www.projectveritas.com/">Project Veritas</a> — erupted in applause.</p>
        <p>Some state officials doubt the influence of these figures in the Garden State, one of the nation’s most diverse. They mention that ultraconservatives are vastly outnumbered here. They point out that far-right candidates have repeatedly lost in statewide races, and voters haven’t elected a Republican senator since 1972 or supported a GOP presidential candidate since 1988.</p>
        <p>“In New Jersey, that doesn't exist,” former Democratic governor and recently retired state Sen. Richard Codey told NJ Advance Media.</p>
        <p>But the GOP did <a href="https://www.nj.com/politics/2021/11/what-the-hell-just-happened-in-new-jersey-how-the-2021-election-redefined-crazy.html">shake up the state in 2021</a>, narrowly losing the gubernatorial election. Three years later, Trump’s rally in Wildwood drew 80,000 to 100,000 people, according to Lisa Fagan, spokesperson for the city.</p>
        <p>“There's this anti-establishment feeling, which the party has always had an element of … and it's getting stronger,” said Mike DuHaime, a Republican operative who served as senior advisor to former Gov. Chris Christie's presidential campaign.</p>
        <p>“I guess I'll wait to see the success before I really judge what it is,” DuHaime added. “Is it a group that does big rallies or is it a group that wins elections?”</p>
        <p>But far-right Republicans have won plenty of school board races, said Micah Rasmussen, director of the Rebovich Institute for New Jersey Politics at Rider University.</p>
        <p>It shows they’re making progress, at least at the local level —  where the state’s political leaders of the future are bred, he said. And perhaps it’s evidence that the Republican rank-and-file has begun turning on the GOP establishment as it has in many other states in favor of far-right voices.</p>
        <p>“The party so far has continued to put up moderate statewide candidates like Jack Ciattarelli, like Bob Hugin … but I certainly think that the Ed Durrs of the world are winning … They're becoming the face of the party,” Rasmussen said.</p>
        <p>“If you're asking me where do we stand in the fight for the soul of the Republican Party in New Jersey, I don't think the Trump wing is there yet,” he added. “But they're certainly working it night and day.”</p>
        <p>That includes trying to move into the political mainstream.</p>
        <p>Crispi is part of a new generation of MAGA conservatives — like Charlie Kirk and Andrew Tate — using digital influence to expand their reach.</p>
        <p>Last year, <a href="https://salempodcastnetwork.com/podcasts/mike-crispi-unafraid">"Mike Crispi Unafraid"</a> was acquired by Salem Media Group, a growing powerhouse in Christian and conservative content. Crispi is also close with Trump, often posting photos on social media from Trump Tower or Mar-a-Lago. And he’s been seen with and endorsed by Roger Stone, a Trump consultant and Republican operative <a href="https://www.washingtonpost.com/opinions/2019/01/27/how-did-roger-stone-survive-watergate/">tied to the Watergate scandal.</a></p>
        <p>Another example is Edward Durfee, a Bergen County Oath Keeper and leader of its northern New Jersey chapter, who ran for the state Assembly after the Capitol riot and lost.</p>
        <p>He also serves as chairman of the Northvale Republican Party Committee.</p>
        <p>Durfee and the rest of the local Oath Keepers — an ultraconservative anti-government organization — maintained a lower profile in the aftermath of the Jan. 6 riot. Members were “very scared of the tyranny” that followed, said Durfeee, referring to the arrests and prosecutions of those who participated in the insurrection. He was at the Capitol that day, but was not arrested.</p>
        <p>“As the quote-unquote leader for New Jersey, I haven’t called a meeting just with all the controversy that’s been going on,” he told NJ Advance Media in April.</p>
        <p>But he remains involved on the local level trying to get Republican candidates elected.</p>
        <p>And he’s open to running for office again, he says.</p>
    </div>
</div>
