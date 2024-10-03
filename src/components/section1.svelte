<script>
    import '../styles/section-styles.css';
    import info1 from '$lib/assets/ch-1-chart.png';
    import video1 from '$lib/assets/Extreme_intro3.mp4';
    import chIco from '$lib/assets/rino.png';
    import TreeModal from './info-modal.svelte';
    import crispi from '$lib/assets/crispi.jpg';
    import soloway from '$lib/assets/soloway.jpg';
    import spadea from '$lib/assets/spadea.png';
    import image1 from '$lib/assets/ch1-img.jpg';
    
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
    <h3> Chapter 1 </h3>
    <h4> A Dark Cloud </h4>
  </div>
    <div>
      <p><span class="drop-cap">T</span>hey gathered at a former daycare center, tucked on a rural road in the Pine Barrens.</p>

      <p>American flags and Trump signs hung on off-white walls. A fluorescent yellow placard, bearing a rhinoceros silhouette, leaned against the lectern. It read, “Please stop feeding the RINOS” — Republicans In Name Only.</p>
      
      <p>An unsettling buffet of conspiracy and grievance followed.</p>
      
      <p>Democrats are grooming your children, speakers told the audience of 40 or so, seated in mismatched metal folding chairs.</p>
      
      <p>The 2020 election was stolen.</p>
      
      <p>Liberals will do it again in November if you don’t serve as poll monitors.</p>
      
      <p>Then a polished man in a fashionable blue suit and black-rimmed glasses strolled to the front of the spacious room. The keynote speaker apologized for being tired that March evening in Shamong before launching into his fundamental issue.</p>
      
      <p>Migrants.</p>
      
      <p>Specifically, the “vermin” and “slime” coming into the United States.</p>
      
      <p id="soloway">“They're bringing in more than crime,” 
        <TreeModal 
        name={"Dr. Stephen Soloway"}
        facts={["Vineland-based rheumatologist", "Author of “Medical Politics: How to Protect Yourself from Bad Doctors, Insurance Companies, and Big Government” and “Bad Medicine: The Horrors of American Healthcare”", "Appointed to the president's Council on Sports, Fitness and Nutrition by former President Trump"]}
        treeTop={[{ name: "Americas First Republican Party", link: null }]} 
        treeMid={[{ name: "Donald Trump", link: null, main: false }, { name: "Dr. Stephen Soloway", link: null, main: true }, { name: "Rep Bob Auth", link: "#auth", main: false }]} 
        treeBottom={[]}
        imageUrl={soloway}
      >
        
        <span class="highlight" title="Click to learn more about this character">Dr. Stephen Soloway</span>
      </TreeModal> 
        , a rheumatologist based in Vineland and a longtime friend of former President Donald Trump, told the audience. “They're bringing in more than rape. They're bringing in something invisible. They're bringing in diseases.”</p>
      
      <p>A dozen or so applauded Soloway as state Assemblyman Bob Auth (R-Bergen) and others looked on from the back.</p>
      
      <p>The event — billed as a “Hands Off My Ballot” rally open to the public — was hosted by two influential organizations: the America First Republicans of New Jersey and the New Jersey Project.</p>
      
      <p>These grassroots groups are part of a loose confederation of far-right influencers that have somehow found an audience in New Jersey, long viewed as a left-leaning bastion of pragmatic politics. And they’ve largely done it using hate speech, bigotry and discord.</p>
      
      <p>They are engineering outrage, weaponizing cultural issues, and sowing division and distrust, NJ Advance Media has found in a nine-month investigation of the Garden State’s burgeoning ultraconservative movement. These influencers are wielding conspiracy theories, intolerance and scapegoating while mainstreaming extremism by hijacking conventional political issues.</p>
      
      <p>All the while, state Republicans are turning a blind eye or even supporting the movement to satisfy a growing far-right base as we approach maybe the most divisive presidential election in American history.</p>
      
      <p>“Even in New Jersey, they are latching on to these populous talking points of: ‘It’s the other guy.’ It’s the fear of the other,” said a state Democratic official not authorized to speak for the party.</p>
      
      <p>“It’s a tale as old as time.”</p>
      
      <div class="video-container">
        <video bind:this={video} src={video1} autoplay loop muted>
          <track kind="captions" />
        </video>
        <button class="mute-button" on:click={toggleMute}>
          {isMuted ? 'Unmute' : 'Mute'}
        </button>
      </div>
      
      <p>Beginning in February, we attended events ranging from pro-Trump rallies to fundraisers for Jan. 6 rioters to church movie nights and found overtly xenophobic and anti-LGBTQ+ rhetoric and even white supremacist messaging. We also monitored social media accounts and podcasts and interviewed more than three dozen politicians, political insiders and experts, examining the pockets of extremism that have developed in New Jersey in the aftermath of the 2016 presidential election and the Jan. 6, 2021 Capitol riot.</p>
      
      <p>Some groups, such as the America First Republicans and Concerned Citizens of NJ, are polarizing and inflaming voters and casting doubt on democratic institutions, including the GOP itself. They’re also employing scare tactics, borrowing talking points from Russian state television and normalizing racist and white nationalist rhetoric, our investigation found. And these toxic influencers are manipulating education issues to rally support for far-right causes and venerating Jan. 6 rioters in a state where more than 40 people were arrested for their alleged roles in the insurrection.</p>
      
      <p>They are increasingly operating out in the open in New Jersey, despite their corrosive language, looking nothing like the people most would associate with conventional notions of extremism.</p>
      
      <p>The ultraconservative wing is a “dark cloud” hovering over the state GOP, a high-ranking Republican operative who runs campaigns told NJ Advance Media. Its hateful rhetoric is viewed as a necessary evil that party officials refuse to confront — and sometimes even embrace — out of fear of losing support in the Trump era, said the official, who was not authorized to speak for the party.</p>
      
      <p>It’s a “coalition of the willing,” said Jon Lewis, an extremism expert at George Washington University.</p>
            
      <p id="crispi">Although some of these figures have a limited sphere of influence, a few — like 
        <TreeModal 
        name={"Mike Crispi"}
        facts={["Failed congressional candidate", "Host of “Mike Crispi Unafraid”", "Chairman of the America First Republicans of New Jersey"]}
        treeTop={[{ name: "Americas First Republican Party", link: null }]} 
        treeMid={[{ name: "Mike Crispi", link: null, main: true }, { name: "Dr. Stephen Soloway", link: "#soloway", main: false }]} 
        treeBottom={[]}
        imageUrl={crispi}
      >
        <span class="highlight" title="Click to learn more about this character">Crispi</span>
      </TreeModal>
      and Spadea, a 101.5 FM drive-time talk show host — are among the most powerful conservative influencers in the state.</p>

      
      <p>And they are part of a larger mission, a number of political insiders and experts tell NJ Advance Media. They want to: push the state’s Republican Party to the right, coalesce support at the grassroots level, win municipal, school board and county elections in a state that leans strongly left and develop future political candidates for higher office.</p>
      
      <p>Many of the same ultraconservative influencers endorse each other, cross-promote each other’s events on social media and act as dignitaries at those gatherings, delivering speeches, amplifying messaging and crowdsourcing fundraising efforts.</p>
      
      <p>They range from fringe operatives to gubernatorial candidates to influential insiders with direct access to Trump. They are people like Mike Crispi, 31, the charismatic rock star of the group. The co-chair of the America First Republicans of New Jersey and a former Congressional candidate received a shoutout from the former president in May after being selected to speak at Trump’s Wildwood campaign rally.</p>
      
      <p>But Crispi has targeted migrants and the trans community on his “Mike Crispi Unafraid” syndicated livestream and pushed <a href="https://www.splcenter.org/hatewatch/2022/05/17/racist-great-replacement-conspiracy-theory-explained">the Great Replacement theory</a> — which claims the white population is being systematically replaced by people of color in a grand conspiracy. In an August episode, Crispi used racist tropes to attack <a href="https://rumble.com/v59brdp-trump-exposes-kamalas-worst-secret-her-poll-numbers-will-now-tank-8pm.html">presidential candidate Kamala Harris</a>, labeling her a “DEI hire.”</p>
      
      <p>“Obviously our country is an unrecognizable state. I think there are good people who need a voice, who need to be defended,” he told NJ Advance Media last month in his signature raspy voice at a “Too Big To Rig” event at a Paramus VFW. “I think it's a battle of good versus evil right now.”</p>
      
      <p>Crispi is far from alone in this web of influencers. We also encountered:</p>
      <ul>
      <li>Ed Durr, the <a href="https://www.nj.com/politics/2021/11/a-newly-elected-nj-state-senator-shocked-the-political-world-then-donald-trump-called.html">truck driver turned GOP sensation</a> who stunned the political world, ousting state Senate President Stephen Sweeney from the Legislature in 2021.</li>
      
      <li id="spadea">
        
        <TreeModal 
      name={"Bill Spadea"}
      facts={["Host of the morning show on New Jersey 101.5 and anchor of 'Chasing News'", "2025 gubernatorial candidate", "Endorsed Mike Crispi"]}
      treeTop={[{ name: "LINK HERE", link: null }]}   
      treeMid={[{ name: "Bill Spadea", link: null, main: true }, { name: "LINK HERE", link: null, main: false }]} 
      treeBottom={[]}
      imageUrl={spadea}
    >
      <span class="highlight" title="Click to learn more about this character">Spadea</span>
    </TreeModal>
        
        , an election denier and COVID vaccine conspiracy theorist, who's using his <a href="https://www.nj.com/politics/2024/06/pro-trump-radio-host-jumps-into-nj-governors-race.html">radio show as a pulpit</a> to run for governor in 2025.</li>
      
      <li>New York attorney <a href="https://theintercept.com/2024/07/18/nick-fuentes-america-first-conference/">Paul Ingrassia</a>, a Substack writer and member of the New York Young Republican Club who supports <a href="https://www.newsweek.com/laura-loomer-message-haters-donald-trump-nothing-lose-1954873">Laura Loomer</a>, a self-described white nationalist and Islamophobe.</li>
      
      <li id="hughes">
        <TreeModal 
      name={"Cynthia Hughes"}
      facts={["Founder and president of The Hughes-Foundation and the Patriot Freedom Project", "Adoptive aunt of Jan. 6 Capitol rioter Timothy Hale-Cusanelli"]}
      treeTop={[{ name: "Donald Trump", link: null }]} 
      treeMid={[{ name: "Cynthia Hughes", link: null, main: true }, { name: "Timothy Hale-Cusanelli", link: null, main: false }]} 
      treeBottom={[]}
    >
      <span class="highlight" title="Click to learn more about this character">Cynthia Hughes</span>
    </TreeModal>
        
        a New Jersey aunt of a U.S. Capitol rioter who has raised millions for the legal defense of Jan. 6 defendants through her <a href="https://patriotfreedomproject.com/">Patriot Freedom Project.</a></li>
      
      <li id="carlos">Union County Republican Party chair 
        
        <TreeModal 
      name={"Carlos Santos"}
      facts={["Union County Republican chair", "Endorsed by Mike Crispi and Paul Ingrassia"]}
      treeTop={[{ name: "Concerned Citizens of New Jersey", link: null }]}   
      treeMid={[{ name: "Carlos Santos", link: null, main: true }, { name: "Lee Mack", link: null, main: false }]} 
      treeBottom={[]}
    >  
      <span class="highlight" title="Click to learn more about this character">Carlos Santos</span>
    </TreeModal>
        
        , a former ironworker who ousted the establishment chair in June and preaches inclusion while promoting figures like Lee Mack.</li>

      <li>Mack espouses conspiracy theories, anti-LGBTQ+ messaging and Russian propaganda through his <a href="https://www.concernedcitizensnj.org/">Concerned Citizens of New Jersey</a> group.</li>
      
      <li>Nicole Stouffer, co-founder of <a href="https://newjerseyproject.org/">the New Jersey Project</a>, a parental rights group <a href="https://www.nj.com/education/2024/06/8-nj-parents-groups-labeled-anti-government-on-new-list-by-hate-watchdog-organization.html">named an anti-government organization</a> by the Southern Poverty Law Center.</li>
      
      <li>Elected officials like Auth, Englishtown Mayor Daniel Francisco and Keyport Mayor Rose Araneo.</li>
      
      </ul>
      <p>“These guys all sit in the same cesspool. There's never more than one or two degrees of separation,” Lewis said.</p>
      
      <img alt="artistic rendering of a political rally" src={image1}>

      <p>They are reaching tens of thousands of people, despite rhetoric filled with conspiracy theories, election denial and hate speech targeting vulnerable communities.</p>
      
      <p>The most persuasive influencers are those with political commentary platforms who frame their rhetoric as conventional political discourse and existential threats, according to Elizabeth Neumann, the former assistant secretary for counterterrorism and threat prevention at the U.S. Department of Homeland Security under Trump.</p>
      
      <p>She is among the officials who fear the result will be politically motivated violence.</p>
      
      <p>“The rhetoric and the tension in the country is still at all-time highs,” Neumann said. “And just based on past precedents, we do expect we are going to see violence this year.”</p>
      
      <p>But these influencers are not just operating in Appalachia. Or along the Gulf Coast. Or in the lonely, wind-swept Plains.</p>
      
      <p>They’re thriving here in New Jersey.</p>
  </div>
</div>

<style>
  .video-container {
    width: 100vw;
    margin-left: calc(-50vw + 50%);
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
</style>