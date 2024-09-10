<script>
    import { onMount } from 'svelte';

    // Function to draw a line between two points
    function drawLine(x1, y1, x2, y2, color = 'darkgray') {
        const line = document.createElementNS('http://www.w3.org/2000/svg', 'line');
        line.setAttribute('x1', x1);
        line.setAttribute('y1', y1);
        line.setAttribute('x2', x2);
        line.setAttribute('y2', y2);
        line.setAttribute('stroke', color);
        line.setAttribute('stroke-width', '2');
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

        // Draw initial lines between all boxes
        boxes.forEach((box1, index1) => {
            const rect1 = box1.getBoundingClientRect();
            const x1 = rect1.left + rect1.width / 2;
            const y1 = rect1.top + rect1.height / 2 - containerTop; // Adjust for container offset

            boxes.forEach((box2, index2) => {
                if (index1 !== index2) {
                    const rect2 = box2.getBoundingClientRect();
                    const x2 = rect2.left + rect2.width / 2;
                    const y2 = rect2.top + rect2.height / 2 - containerTop; // Adjust for container offset

                    const line = drawLine(x1, y1, x2, y2);
                    svg.appendChild(line);
                    lines.push({ line, box1, box2 });
                }
            });
        });

        // Add click event listeners to boxes
        boxes.forEach((box) => {
            box.addEventListener('click', () => {
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
    <h3>How Are these People connected?</h3>
    <h4>Here is room for a subtitle of description</h4>
    <p>Click to highlight connections with others</p>
</div>
<div class="chart-container">
    <div class="r-1 bill box">
        <p>Bill Spadea</p>
        <ul>
            <li>Radio talk show host - 101.5</li>
            <li>2025 gubernatorial candidate</li>
            <li>Conspiracy theorist, election denier</li>
            <li>Listed on Crispi's website as an endorser</li>
            <li>Appeared at Carlos Santos fundraiser</li>
            <li>Endorsed Ed Durr for State Senate</li>
        </ul>
    </div>
    <div class="r-1 roger box">
        <p>Roger Stone</p>
        <ul>
            <li>Far right activist with clost ties to Trump</li>
        </ul>
    </div>
    <div class="r-2 laura box">
        <p>Laura Loomer</p>
        <ul>
            <li>far-right white nationalist, conspiracy theroist and self described "Islamophobe"</li>
            <li>seen in numerous photos with Crispi and Ingrassia</li>
        </ul>
    </div>
    <!--row 3-->
    <div class="r-2 ed box">
        <p>Ed Durr</p>
        <ul>
            <li>Former State senator</li>
            <li>Spoke at Shamog event with Nik</li>
            <li>Appeaerd at Carlos Santos' fundraiser</li>
        </ul>
    </div>
    <div class="r-3 bob box">
        <p>Bob Auth</p>
        <ul>
            <li>New Jersey Republican Assemblyman</li>
            <li>Spoke at America First events</li>
            <li>Spoke at Shamog Event with Nik Stouffer, Ed Durr, and Sephen Soloway</li>
        </ul>
    </div>
    <div class="r-3 stephen box">
        <p>Dr Stephen Soloway</p>
        <ul>
            <li>Vineland baised doctor</li>
            <li>Appointed to the presidents council on sports, fitness, and Nutrition by former presicent Trump</li>
            <li>Spoke at Shamong event, spouting anti-immagrant rehetoric</li>
            <li>Has raised money for Jeff Van Drew</li>
        </ul>
    </div>
    <div class="r-3 cynthia box">
        <p>Cynthia Hughes</p>
        <ul>
            <li>Adoptive aunt of Jan 6 Rioter</li>
            <li>Founder of the Patriot Freedom Project</li>
            <li>Spoke at AFRNJ event in Keyport with Crispi and Ingrassia</li>
        </ul>
    </div>
        <!--row 2-->
        <div class="r-4 mike box">
            <p>Mike Crispi</p>
            <ul>
                <li>Onine talk show host</li>
                <li>co-chair of America First Republicans for NJ</li>
                <li>Conspiracy theroist, election denier</li>
                <li>Has promoted the "great replacment theory" on his talk show</li>
            </ul>
        </div>
    <div class="r-5 paul box">
        <p>Paul Ingrassia</p>
        <ul>
            <li>New Yorker with links to Crispi, Roger Stone, and Loomer</li>
            <li>He appeared at America First Event with Crispi</li>
            <li>Linked to the McBride law firm</li>
            <li>Sent a video endorsement at Carlos Santos event in Feb</li>
        </ul>
    </div>
    <!--row 4-->
    <div class="r-5 jeff box">
        <p>Rep. Jeff Van Drew</p>
        <ul>
            <li>MAGA Congressman</li>
            <li>In charge of Trump's NJ campaign</li>
            <li>Election denier</li>
            <li>Has appeared with Crispi and AFRNJ</li>
        </ul>
    </div>
    <div class="r-5 nik box">
        <p>Nik Stouffer/ The New Jersey Project</p>
        <ul>
            <li>Co-founder of the NJ Project, a parental rights group that promotes book-banning and anti-LGBTQ rehetoric</li>
            <li>Has hosted event with CCNJ</li>
        </ul>
    </div>
    <div class="r-6 carlos box">
        <p>Carlos Santos</p>
        <ul>
            <li>Has Fundraised with America first Republicans of NJ</li>
            <li>Linked to Crispi and Ingrassia</li>
            <li>Became union County Republican chair</li>
            <li>Lists a host of Far-right extreme ideas on his website</li>
            <li>lists CCNJ on his website</li>
        </ul>
    </div>
    <!--row 5-->
    <div class="r-6 lee box">
        <p>Lee Mack</p>
        <ul>
            <li>Runs Concerned Citizens of NJ, a small grassroots nonprofit that promotes overt conspiracy theories and anti-semitic tropes</li>
            <li>has ties with Stouffer and has co-hosted events with the New Jersey Project</li>
        </ul>
    </div>
    <div class="r-6 phil box">
        <p>Pastor Phil Maxwell</p>
        <ul>
            <li>Head of Gateway church (where Lee Mack will hold gatherings for CCNJ)</li>
            <li>antisemitic sermons</li>
        </ul>
    </div>
</div>

<style>
    .chart-title{
        text-align: center;
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
        padding: 0 10px;
        margin: 0 10px;
        width: 100vw;
        margin: 0
    }

    .chart-title p {
        font-size: 12px;
        margin: 20px 0;
    }

    p{
        font-family: 'Courier New', Courier, monospace;
        text-align: center;
        margin-top: 0;

    }

    ul{
        list-style: none;
        font-family: Arial, Helvetica, sans-serif;
        font-size: 7pt;
        padding-left: 0;
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
    .phil { grid-column: 6/7; }
</style>
