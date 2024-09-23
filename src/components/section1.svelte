<script>
    import '../styles/section-styles.css';
    import info1 from '$lib/assets/ch-1-chart.png';
    import video1 from '$lib/assets/Extreme_intro.mp4';
    import info2 from '$lib/assets/Frame 6.png';
    import chIco from '$lib/assets/rino.png';
    import TreeModal from './info-modal.svelte';
    import Chart from './chart.svelte';
    
    let video;
  let isMuted = true;

  function toggleMute() {
    if (video) {
      video.muted = !video.muted;
      isMuted = video.muted;
    }
  }
  </script>
    
<div class="section-container">
  <div class="section-title">
    <img class="ch-icon" src={chIco} alt="republician elephant"/>
    <h3> Section 1 </h3>
    <h4> Placeholder Title </h4>
  </div>
    <div>
    <p> <span class="drop-cap">T</span>he meeting was an unsettling buffet of conspiracy and grievance.</p>
    <p>They had gathered at a former daycare center, tucked on a rural road in the Pine Barrens. American flags and Trump signs hung on off-white walls. A fluorescent yellow placard, bearing a rhinoceros silhouette, leaned against the lectern. It read, “Please stop feeding the RINOS” — Republicans In Name Only.</p>
    <p>Four speakers then took turns riling up the Shamong audience of 40 or so, seated in mismatched metal folding chairs.</p>
    <p>Democrats are grooming your children, they said. The 2020 election was stolen. Liberals will do it again in November if you don’t serve as poll monitors.</p>
    <p>Then a polished man in a fashionable blue suit and designer, black-rimmed glasses strolled to the front of the spacious room that Friday evening in March. He apologized for being tired before launching into his key issue.</p>
    <p>Migrants. Specifically, the “vermin” and “slime” coming into the United States.</p>
    <p id="soloway">“They're bringing in more than crime,” 
      <TreeModal 
      name={"Dr. Stephen Soloway"}
      facts={["Vineland-based rheumatologist", "Author of “Medical Politics: How to Protect Yourself from Bad Doctors, Insurance Companies, and Big Government” and “Bad Medicine: The Horrors of American Healthcare”", "Appointed to the president's Council on Sports, Fitness and Nutrition by former President Trump"]}
      treeTop={[{ name: "Americas First Republican Party", link: null }]} 
      treeMid={[{ name: "Donald Trump", link: null, main: false }, { name: "Dr. Stephen Soloway", link: null, main: true }, { name: "Rep Bob Auth", link: "#auth", main: false }]} 
      treeBottom={[]}
    >
      
      <span class="highlight" title="Click to learn more about this character">Dr. Stephen Soloway</span>
    </TreeModal> 
      , a rheumatologist based in Vineland and a longtime friend of former President Donald Trump, told the audience. “They're bringing in more than rape. They're bringing in something invisible. They're bringing in diseases.”</p>
    <p>A dozen or so applauded Soloway, the keynote speaker, as state Assemblyman Bob Auth (R-Bergen) and others looked on from the back.</p>    
    <p>The event — billed as a “Hands Off My Ballot��� rally and open to the public — was hosted by two influential organizations: the America First Republicans of New Jersey and the New Jersey Project, a parental rights collective named an anti-government organization this year by the Southern Poverty Law Center.</p>
    <p>These grassroots groups are among a loose confederation of far-right influencers and organizations that have somehow found an audience in New Jersey, long celebrated as a left-leaning bastion of pragmatic politics. And they’ve done it using hate speech, bigotry and rage.</p>
    <p>“Even in New Jersey, they are latching on to these populous talking points of: ‘It’s the other guy.’ It’s the fear of the other,” said a state Democratic official not authorized to speak for the party. “It’s a tale as old as time.”</p>
    <img alt="info rally" src={info1}>
    <p>These influencers are engineering outrage, weaponizing cultural issues, and sowing division and distrust in traditionally levelheaded New Jersey, NJ Advance Media has found in a nine-month investigation of the Garden State’s burgeoning ultraconservative movement. They are attempting to mainstream extremism by hijacking conventional political issues and portraying them through the prism of conspiracy theories, discrimination and scapegoating as we approach maybe the most divisive presidential election in American history, our investigation found. All the while, moderate state Republicans are turning a blind eye or even supporting the movement to satisfy their base.</p>
    <p>We attended events ranging from pro-Trump rallies to fundraisers for Jan. 6 rioters to church movie nights and found overtly xenophobic, antisemitic and anti-LGBTQ+ rhetoric at many of them — complete with white supremacist overtones. We also monitored social media accounts, podcasts and internet forums and interviewed xx politicians, law enforcement officials, political insiders and experts, examining the pockets of extremism that have developed in New Jersey in the aftermath of the 2016 presidential election and the Jan. 6, 2021 Capitol riot.</p>
    <p>Some groups, such as the America First Republicans and Concerned Citizens of NJ, are pulling the strings of New Jersey’s political fury, polarizing and inflaming voters and casting doubt on democratic institutions, including the GOP itself. They’re employing scare tactics, borrowing talking points from Russian state television and trying to normalize racist and white nationalist rhetoric, our investigation found. And these toxic influencers are manipulating geopolitical, religious and education issues on a grassroots level to seed discord and rally support for far-right causes.</p>
    <p>The ultraconservative wing is a “dark cloud” hovering over the state GOP, a high-ranking Republican operative who runs campaigns told NJ Advance Media. Their hateful rhetoric is viewed as a necessary evil that party officials refuse to confront – and sometimes even embrace — out of fear of losing support in the Trump era, said the official, who requested anonymity because they are not authorized to speak for the party.</p>
    <div class="video">
      <video bind:this={video} src={video1} autoplay loop muted>
        <track kind="captions" />
      </video>
      <button class="mute-button" on:click={toggleMute}>
        {isMuted ? 'Unmute' : 'Mute'}
      </button>
    </div>
    <p>It’s a “coalition of the willing,” said Jon Lewis, an extremism expert at George Washington University.</p>
    <p>These far-right organizations are part of a larger plan, a number of political insiders and experts tell NJ Advance Media. They have four distinct objectives: 1. Push the state’s Republican Party to the right, 2. Coalesce support at the grassroots level, 3. Win municipal and county elections and 4. Develop future political candidates for higher office.</p>
    <p>Many of the same ultraconservative influencers cross-promote each other’s gatherings on social media and act as dignitaries at those events, delivering speeches and amplifying messaging.</p>
    <p id="crispi">They are podcasters, political organizers, gubernatorial candidates and deeply connected insiders with direct access to Trump. They are people like
      <TreeModal 
      name={"Mike Crispi"}
      facts={["Failed congressional candidate", "Host of “Mike Crispi Unafraid”", "Chairman of the America First Republicans of New Jersey"]}
      treeTop={[{ name: "Americas First Republican Party", link: null }]} 
      treeMid={[{ name: "Mike Crispi", link: null, main: true }, { name: "Dr. Stephen Soloway", link: "#soloway", main: false }]} 
      treeBottom={[]}
    >
      <span class="highlight">Mike Crispi</span>
    </TreeModal>
    , the charismatic xxx31-year-oldxxx rock star of the group, who received a shoutout from Trump in May at the former president’s Wildwood rally. The well-dressed political activist with a signature raspy voice speaks fast and fervently. His bellicose manner energizes crowds when speaking as the chairman of the America First Republicans of New Jersey and galvanizes listeners of his syndicated podcast, “Mike Crispi Unafraid.”</p>
    <p>In one episode, he barely took a breath between words: “It seems like the illegal vermin — I keep calling them vermin, and people keep saying, ‘Oh, that’s racist, it’s this, it’s that.’ But here’s the thing: It couldn’t be any further from reality.”</p>
    <p id="Hughes">But Crispi is far from alone. There’s Tim Walsh, Mike Casey and Mike Byrne — members of the America First Republicans of New Jersey. There’s also <span>Ed Durr</span>, the truck driver turned GOP sensation who ousted state Senate President Stephen Sweeney from the Legislature in 2021, NJ1st podcaster Ryan McDonald and New York attorney Paul Ingrassia, a Substack writer and member of the New York Young Republican Club. Then there’s 
      <TreeModal 
      name={"Cynthia Hughes"}
      facts={["Founder and president of The Hughes-Foundation and the Patriot Freedom Project", "Adoptive aunt of Jan. 6 Capitol rioter Timothy Hale-Cusanelli"]}
      treeTop={[{ name: "Donald Trump", link: null }]} 
      treeMid={[{ name: "Cynthia Hughes", link: null, main: true }, { name: "Timothy Hale-Cusanelli", link: null, main: false }]} 
      treeBottom={[]}
    >
      <span class="highlight">Cynthia Hughes</span>
    </TreeModal>
      , a New Jersey mother and adoptive aunt of a U.S. Capitol rioter who has raised millions for the legal defense of Jan. 6 defendants — and become a Trump favorite in the process.</p>
    <p id="spadea">You’ll also see political operatives like Union County Republican Party chair Carlos Santos and elected officials like Auth and Englishtown Mayor Daniel Francisco. And you’ll encounter popular 101.5 talk show host 
      <TreeModal 
      name={"Bill Spadea"}
      facts={["Host of the morning show on New Jersey 101.5 and anchor of 'Chasing News'", "2025 gubernatorial candidate", "Endorsed Mike Crispi"]}
      treeTop={[{ name: "LINK HERE", link: null }]}   
      treeMid={[{ name: "Bill Spadea", link: null, main: true }, { name: "LINK HERE", link: null, main: false }]} 
      treeBottom={[]}
    >
      <span>Bill Spadea</span>
    </TreeModal>
      , an election denier and COVID vaccine conspiracy theorist who's running for governor in 2025.</p>
    <p>”The biggest influencers, the ones with the massive platforms, are sometimes politicians, and often people with political commentary platforms,” said Elizabeth Neumann, the former assistant secretary for counterterrorism and threat prevention at the U.S. Department of Homeland Security under Trump.</p>
    <p>“And they frequently frame political rhetoric as political conversation and very existential threats.”</p>
    <p id="santos">Some figures, like Auth, appear to be cynically chumming for support in the most extreme elements of the party. Others, like Ingrassia, are true believers. He is tied to Laura Loomer, a self-described white nationalist and Islamophobe, and has promoted figures like Jack Posobiec, who has collaborated with white supremacists, according to the Southern Poverty Law Center. Then there are opportunists like
      <TreeModal 
      name={"Carlos Santos"}
      facts={["Union County Republican chair", "Endorsed by Mike Crispi and Paul Ingrassia"]}
      treeTop={[{ name: "Concerned Citizens of New Jersey", link: null }]}   
      treeMid={[{ name: "Carlos Santos", link: null, main: true }, { name: "Lee Mack", link: null, main: false }]} 
      treeBottom={[]}
    >  
      <span class="highlight">Santos</span>
    </TreeModal>
      , who promotes activists such as Lee Mack — who hatches conspiracy theories, anti-LGBTQ+ messaging and Russian propaganda through his Concerned Citizens of New Jersey group — while distancing himself from them when questioned by NJ Advance Media.</p>
    <p>These influencers are reaching tens of thousands of people, despite rhetoric filled with conspiracy theories, election denial and hate speech targeting minority groups.</p>
    <p>“These guys all sit in the same cesspool. There's never more than one or two degrees of separation,” Lewis said.</p>
    <p>But they’re not operating in Appalachia. Or the Mississippi Delta. Or the lonely, wind-swept Plains.</p>
    <p>They’re thriving here in New Jersey.</p>
  </div>
</div>

<style>
  .video {
    max-width: 80vw;
    height: auto;
    position: relative;
  }

  video {
    width: 100%;
    height: auto;
  }
  .mute-button {
    position: absolute;
    bottom: 10px;
    right: 10px;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: 5px 10px;
    cursor: pointer;
    font-size: 14px;
    border-radius: 4px;
  }
  .mute-button:hover {
    background-color: rgba(0, 0, 0, 0.7);
  }

  .highlight::after {
    content: attr(title);
    position: absolute;
    bottom: 100%;
    left: 50%;
    transform: translateX(-50%);
    background-color: black;
    color: white;
    padding: 5px;
    border-radius: 3px;
    font-size: 12px;
    white-space: nowrap;
    opacity: 0;
    transition: opacity 0.3s;
    pointer-events: none;
  }

  .highlight:hover::after {
    opacity: 1;
  }
</style>
