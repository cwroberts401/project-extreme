<script>
    import { onMount } from 'svelte';

    // Define connections between specific cards
    const connections = [
        { from: 'nik', to: ['lee', 'bob'] },
        { from: 'mike', to: ['bill', 'ed', 'bob', 'stephen', 'cynthia', 'paul', 'laura','roger', 'nik', 'carlos',  'jeff'] },
        { from: 'lee', to: ['carlos'] },
        { from: 'carlos', to: ['bill', 'ed', 'paul' ] },
        { from: 'jeff', to: ['stephen'] },
        { from: 'bob', to: ['ed', 'stephen'] },
        { from: 'cynthia', to: ['paul'] },
        { from: 'paul', to: ['laura', 'roger'] },
    ];

    // Function to draw a line between two points
    function drawLine(x1, y1, x2, y2, color = 'darkgray') {
        const line = document.createElementNS('http://www.w3.org/2000/svg', 'line');
        line.setAttribute('x1', x1);
        line.setAttribute('y1', y1);
        line.setAttribute('x2', x2);
        line.setAttribute('y2', y2);
        line.setAttribute('stroke', color);
        line.setAttribute('stroke-width', '4'); // Increased line thickness
        return line;
    }

    // Function to generate random rotation
    function getRandomRotation() {
        return Math.floor(Math.random() * 21) - 10; // Random number between -10 and 10
    }

    onMount(() => {
        const container = document.querySelector('.chart-container');
        const svg = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
        svg.style.position = 'absolute';
        svg.style.top = 0;
        svg.style.left = 0;
        svg.style.width = '100%';
        svg.style.height = '100%';
        svg.style.pointerEvents = 'none';
        svg.style.zIndex = '5';
        container.appendChild(svg);

        const containerRect = container.getBoundingClientRect();
        const containerTop = containerRect.top;
        const boxes = Array.from(container.querySelectorAll('.box'));
        const lines = [];

        // Draw lines only between specified connections
        connections.forEach(connection => {
            const fromBox = container.querySelector(`.${connection.from}`);
            const fromRect = fromBox.getBoundingClientRect();
            const x1 = fromRect.left + fromRect.width / 2;
            const y1 = fromRect.top + fromRect.height / 2 - containerTop;

            connection.to.forEach(to => {
                const toBox = container.querySelector(`.${to}`);
                const toRect = toBox.getBoundingClientRect();
                const x2 = toRect.left + toRect.width / 2;
                const y2 = toRect.top + toRect.height / 2 - containerTop;

                const line = drawLine(x1, y1, x2, y2);
                svg.appendChild(line);
                lines.push({ line, box1: fromBox, box2: toBox });
            });
        });

        // Add click event listeners to boxes
        boxes.forEach((box) => {
            box.addEventListener('click', () => {
                boxes.forEach(b => b.style.zIndex = '10'); // Set all boxes to default z-index
                box.style.zIndex = '100';
                lines.forEach(({ line, box1, box2 }) => {
                    if (box === box1 || box === box2) {
                        line.setAttribute('stroke', 'red');
                        line.setAttribute('opacity', '1');
                    } else {
                        line.setAttribute('stroke', 'darkgray');
                        line.setAttribute('opacity', '0.2');
                    }
                });
            });
        });

        // Add random rotation to each box
        boxes.forEach((box) => {
            const rotation = getRandomRotation();
            box.style.transform = `rotate(${rotation}deg)`;
        });
    });
</script>


<div class="chart-title">
    <h3>How Are These Influencers Connected?</h3>
    <h4>A loose web of political figures leads the far-right movement in New Jersey.</h4>
    <h5><i>Click on the cards to see how each influencer is connected to the others.</i></h5>
</div>
<div class="chart-container">
    <div class="r-1 bill box">
        <p>Bill Spadea</p>
        <div class="dividing-line"></div>
        <ul>
            <li>101.5 radio talk show host</li>
            <li>2025 gubernatorial candidate</li>
            <li>Conspiracy theorist and election denier</li>
            <li>Listed as an endorser on Mike Crispi’s website</li>
            <li>Appeared at a Carlos Santos fundraiser</li>
            <li>Endorsed Ed Durr for state Senate</li>
        </ul>
    </div>
    <div class="r-1 roger box">
        <p>Roger Stone</p>
        <div class="dividing-line"></div>
        <ul>
            <li>Far-right activist who served as an adviser to Donald Trump’s 2016 presidential campaign</li>
            <li>Has close ties to Mike Crispi</li>
        </ul>
    </div>
    <div class="r-2 laura box">
        <p>Laura Loomer</p>
        <div class="dividing-line"></div>
        <ul>
            <li>Far-right white nationalist, conspiracy theorist and self-described "Islamophobe"</li>
            <li>Has been seen in numerous photos with Mike Crispi and Paul Ingrassia</li>
        </ul>
    </div>
    <!--row 3-->
    <div class="r-2 ed box">
        <p>Ed Durr</p>
        <div class="dividing-line"></div>
        <ul>
            <li>Former state senator</li>
            <li>Spoke at the Shamong event with Nicole Stouffer, Stephen Soloway and Assemblyman Auth</li>
            <li>Spoke at Carlos Santos’ fundraiser</li>
        </ul>
    </div>
    <div class="r-3 bob box">
        <p>Robert Auth</p>
        <div class="dividing-line"></div>
        <ul>
            <li>New Jersey Republican assemblyman</li>
            <li>Listed as a member of the America First Republicans’ host committee</li>
            <li>Spoke at the Shamong event with Nicole Stouffer, Ed Durr and Stephen Soloway</li>
        </ul>
    </div>
    <div class="r-3 stephen box">
        <p>Dr. Stephen Soloway</p>
        <div class="dividing-line"></div>
        <ul>
            <li>Vineland-based rheumatologist</li>
            <li>Appointed to the president’s Council on Sports, Fitness and Nutrition by former President Trump</li>
            <li>Spoke at the Shamong event, spouting anti-immigrant rhetoric</li>
            <li>Has raised money for U.S. Rep. Jeff Van Drew</li>
        </ul>
    </div>
    <div class="r-3 cynthia box">
        <p>Cynthia Hughes</p>
        <div class="dividing-line"></div>
        <ul>
            <li>Adoptive aunt of Jan. 6 Capitol rioter Timothy Hale-Cusanelli</li>
            <li>Founder of the Patriot Freedom Project</li>
            <li>Spoke at the America First Republicans of New Jersey event in Keyport with Mike Crispi and Paul Ingrassia</li>
        </ul>
    </div>
        <!--row 2-->
        <div class="r-4 mike box">
            <p>Mike Crispi</p>
            <div class="dividing-line"></div>
            <ul>
                <li>Online talk show host</li>
                <li>Co-chair of the America First Republicans of New Jersey</li>
                <li>Conspiracy theorist and election denier</li>
                <li>Has promoted the “great replacement” theory on his show</li>
            </ul>
        </div>
    <div class="r-5 paul box">
        <p>Paul Ingrassia</p>
        <div class="dividing-line"></div>
        <ul>
            <li>New Yorker with ties to Mike Crispi, Roger Stone and Laura Loomer</li>
            <li>Has appeared at America First Republicans of New Jersey events</li>
            <li>Linked to The McBride Law Firm</li>
            <li>Endorsed Carlos Santos</li>
        </ul>
    </div>
    <!--row 4-->
    <div class="r-5 jeff box">
        <p>U.S. Rep. Jeff Van Drew (R-2nd Dist)</p>
        <div class="dividing-line"></div>
        <ul>
            <li>In charge of Trump’s New Jersey campaign</li>
            <li>Election denier</li>
            <li>Has appeared with Mike Crispi</li>
        </ul>
    </div>
    <div class="r-5 nik box">
        <p>Nicole Stouffer</p>
        <div class="dividing-line"></div>
        <ul>
            <li>Co-founder of the New Jersey Project, a parental rights group that promotes book-banning and anti-LGBTQ+ rhetoric</li>
            <li>Has hosted events with the America First Republicans of New Jersey and the Concerns Citizens of New Jersey</li>
        </ul>
    </div>
    <div class="r-6 carlos box">
        <p>Carlos Santos</p>
        <div class="dividing-line"></div>
        <ul>
            <li>Has fundraised with the America First Republicans of New Jersey</li>
            <li>Has been endorsed by Mike Crispi and Paul Ingrassia</li>
            <li>Was elected Union County Republican chair</li>
            <li>Promotes the Concerns Citizens of New Jersey on his personal website</li>
        </ul>
    </div>
    <!--row 5-->
    <div class="r-6 lee box">
        <p>Lee Mack</p>
        <div class="dividing-line"></div>
        <ul>
            <li>Runs Concerned Citizens of New Jersey, a grassroots nonprofit that promotes conspiracy theories and antisemitic tropes on its website</li>
            <li>Has ties to Nicole Stouffer and has co-hosted events with the New Jersey Project</li>
        </ul>
    </div>
</div>

<style>
    .chart-title{
        text-align: center;
        color: red;
        max-width: 700px;
        margin: 0 auto;
        padding: 0 20px 5px;
    }

    .chart-title>h3 {
        font-family: "Bebas Neue", sans-serif;
        color: #bd1e2d;
    }

    .chart-title>h4 {
        font-family: "Bebas Neue", sans-serif;
        color: white;
    }

    .chart-title>h5 {
        font-family: Arial, Helvetica, sans-serif;
        font-weight: 300;
        color: white;
    }

    .chart-container {
        position: relative; /* Make sure container is positioned relatively */
        display: grid;
        grid-template-columns: repeat(12, minmax(0, 1fr));
        gap: 40px;
        padding-bottom: 30px;
        padding-top: 30px;
        background-image: url('../lib/assets/corkboard.jpg');
        background-size: cover;
        padding: 0;
        margin: 0 10px;
        width: 100vw;
        max-width: 100vw;
        margin: 0;
        overflow: hidden;
    }

    p{
        font-family: "Bebas Neue", sans-serif;
        text-align: center;
        margin-top: 0;
        font-size: 18px;
    }

    .dividing-line{
        height: 1px;
        width: 100%;
        background-color: #bd1e2d;
        margin: 0;
        padding: 0;
    }

    @media (max-width: 768px) {
        p {
            font-size: 11px;
        }

        .chart-container{
            margin: 0;
            padding: 0;
        }
    }

    ul{
        list-style: circle;
        list-style-position: inside;
        font-family: Arial, Helvetica, sans-serif;
        font-size: 7pt;
        padding-left: 0;
        line-height: 1.5;
    }

    .box {
        background-color: white;
        width: 20vw;
        max-width: 30vw;
        padding: 10px;
        cursor: pointer;
        position: relative;
        z-index: 20;
        border-radius: 4px;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
    }

    .box:hover {
        box-shadow: 3px 3px 8px rgba(0, 0, 0, 0.3);
    }

    h3 {
        font-family: 'Courier New', Courier, monospace;
        text-align: center;
        margin-top: 0;
        margin-bottom: 0;
        font-size: 30px;
    }

    p {
        color: black;
        font-size: 22px;
        font-weight: 600;
    }

    li {
        color: black;
    }

    h4 {
        font-family: 'Courier New', Courier, monospace;
        text-align: center;
        margin-top: 0;
        margin-bottom: 0;
        font-size: 18px;
    }

    .r-1 { grid-row: 1; }
    .r-2 { grid-row: 2; }
    .r-3 { grid-row: 3; }
    .r-4 { grid-row: 4; }
    .r-5 { grid-row: 5; }
    .r-6 { grid-row: 6; }
    .bill { grid-column: 4/5; }
    .roger { grid-column: 7/8; }
    .laura { grid-column: 8/9; }
    .mike { grid-column: 5/6; }
    .ed { grid-column: 3/4; }
    .bob { grid-column: 2/3; }
    .stephen { grid-column: 5/6; }
    .cynthia { grid-column: 9/10; }
    .paul { grid-column: 8/9; }
    .jeff { grid-column: 2/3; }
    .nik { grid-column: 5/6; }
    .carlos { grid-column: 9/10; }
    .lee { grid-column: 2/3; }

    @media (max-width: 768px) {
        .box{ width: 40vw}
        .bill { grid-column: 2/4; }
        .roger { grid-column: 7/9; }
        .laura { grid-column: 6/8; }
        .mike { grid-column: 4/6; }
        .ed { grid-column: 2/4; }
        .bob { grid-column: 1/3; }
        .stephen { grid-column: 4/6; }
        .cynthia { grid-column: 7/9; }
        .paul { grid-column: 7/9; }
        .jeff { grid-column: 1/3; }
        .nik { grid-column: 5/7; }
        .carlos { grid-column: 1/10; }
        .lee { grid-column: 5/7; }
    }
</style>