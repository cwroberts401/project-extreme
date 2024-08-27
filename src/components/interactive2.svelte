<script>
    import { onMount, onDestroy } from "svelte";

    let canvas;
    let ctx;

    const svgIcon = `<?xml version="1.0" encoding="UTF-8"?>
<svg id="Layer_1" data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 26 26">
  <defs>
    <style>
      .cls-1 {
        fill: #df1900;
        stroke-width: 0px;
      }
    </style>
  </defs>
    <rect class="cls-1" x="13" width="1" height="1"/>
  <rect class="cls-1" x="14" width="1" height="1"/>
  <rect class="cls-1" x="15" width="1" height="1"/>
  <rect class="cls-1" x="16" width="1" height="1"/>
  <rect class="cls-1" x="16" y="1" width="1" height="1"/>
  <rect class="cls-1" x="17" y="1" width="1" height="1"/>
  <rect class="cls-1" x="18" y="1" width="1" height="1"/>
  <rect class="cls-1" x="18" y="2" width="1" height="1"/>
  <rect class="cls-1" x="19" y="2" width="1" height="1"/>
  <rect class="cls-1" x="20" y="2" width="1" height="1"/>
  <rect class="cls-1" x="20" y="3" width="1" height="1"/>
  <rect class="cls-1" x="21" y="3" width="1" height="1"/>
  <rect class="cls-1" x="21" y="4" width="1" height="1"/>
  <rect class="cls-1" x="22" y="4" width="1" height="1"/>
  <rect class="cls-1" x="22" y="5" width="1" height="1"/>
  <rect class="cls-1" x="23" y="5" width="1" height="1"/>
  <rect class="cls-1" x="23" y="6" width="1" height="1"/>
  <rect class="cls-1" x="23" y="7" width="1" height="1"/>
  <rect class="cls-1" x="24" y="7" width="1" height="1"/>
  <rect class="cls-1" x="24" y="8" width="1" height="1"/>
  <rect class="cls-1" x="24" y="9" width="1" height="1"/>
  <rect class="cls-1" x="25" y="9" width="1" height="1"/>
  <rect class="cls-1" x="25" y="10" width="1" height="1"/>
  <rect class="cls-1" x="25" y="11" width="1" height="1"/>
  <rect class="cls-1" x="25" y="12" width="1" height="1"/>
  <rect class="cls-1" y="12" width="1" height="1" transform="translate(-12 13) rotate(-90)"/>
  <rect class="cls-1" y="11" width="1" height="1" transform="translate(-11 12) rotate(-90)"/>
  <rect class="cls-1" y="10" width="1" height="1" transform="translate(-10 11) rotate(-90)"/>
  <rect class="cls-1" y="9" width="1" height="1" transform="translate(-9 10) rotate(-90)"/>
  <rect class="cls-1" x="1" y="9" width="1" height="1" transform="translate(-8 11) rotate(-90)"/>
  <rect class="cls-1" x="1" y="8" width="1" height="1" transform="translate(-7 10) rotate(-90)"/>
  <rect class="cls-1" x="1" y="7" width="1" height="1" transform="translate(-6 9) rotate(-90)"/>
  <rect class="cls-1" x="2" y="7" width="1" height="1" transform="translate(-5 10) rotate(-90)"/>
  <rect class="cls-1" x="2" y="6" width="1" height="1" transform="translate(-4 9) rotate(-90)"/>
  <rect class="cls-1" x="2" y="5" width="1" height="1" transform="translate(-3 8) rotate(-90)"/>
  <rect class="cls-1" x="3" y="5" width="1" height="1" transform="translate(-2 9) rotate(-90)"/>
  <rect class="cls-1" x="3" y="4" width="1" height="1" transform="translate(-1 8) rotate(-90)"/>
  <rect class="cls-1" x="4" y="4" width="1" height="1" transform="translate(0 9) rotate(-90)"/>
  <rect class="cls-1" x="4" y="3" width="1" height="1" transform="translate(1 8) rotate(-90)"/>
  <rect class="cls-1" x="5" y="3" width="1" height="1" transform="translate(2 9) rotate(-90)"/>
  <rect class="cls-1" x="5" y="2" width="1" height="1" transform="translate(3 8) rotate(-90)"/>
  <rect class="cls-1" x="6" y="2" width="1" height="1" transform="translate(4 9) rotate(-90)"/>
  <rect class="cls-1" x="7" y="2" width="1" height="1" transform="translate(5 10) rotate(-90)"/>
  <rect class="cls-1" x="7" y="1" width="1" height="1" transform="translate(6 9) rotate(-90)"/>
  <rect class="cls-1" x="8" y="1" width="1" height="1" transform="translate(7 10) rotate(-90)"/>
  <rect class="cls-1" x="9" y="1" width="1" height="1" transform="translate(8 11) rotate(-90)"/>
  <rect class="cls-1" x="9" width="1" height="1" transform="translate(9 10) rotate(-90)"/>
  <rect class="cls-1" x="10" width="1" height="1" transform="translate(10 11) rotate(-90)"/>
  <rect class="cls-1" x="11" width="1" height="1" transform="translate(11 12) rotate(-90)"/>
  <rect class="cls-1" x="12" width="1" height="1" transform="translate(12 13) rotate(-90)"/>
  <rect class="cls-1" x="12" y="25" width="1" height="1" transform="translate(25 51) rotate(180)"/>
  <rect class="cls-1" x="11" y="25" width="1" height="1" transform="translate(23 51) rotate(180)"/>
  <rect class="cls-1" x="10" y="25" width="1" height="1" transform="translate(21 51) rotate(180)"/>
  <rect class="cls-1" x="9" y="25" width="1" height="1" transform="translate(19 51) rotate(180)"/>
  <rect class="cls-1" x="9" y="24" width="1" height="1" transform="translate(19 49) rotate(180)"/>
  <rect class="cls-1" x="8" y="24" width="1" height="1" transform="translate(17 49) rotate(180)"/>
  <rect class="cls-1" x="7" y="24" width="1" height="1" transform="translate(15 49) rotate(180)"/>
  <rect class="cls-1" x="7" y="23" width="1" height="1" transform="translate(15 47) rotate(180)"/>
  <rect class="cls-1" x="6" y="23" width="1" height="1" transform="translate(13 47) rotate(180)"/>
  <rect class="cls-1" x="5" y="23" width="1" height="1" transform="translate(11 47) rotate(180)"/>
  <rect class="cls-1" x="5" y="22" width="1" height="1" transform="translate(11 45) rotate(180)"/>
  <rect class="cls-1" x="4" y="22" width="1" height="1" transform="translate(9 45) rotate(180)"/>
  <rect class="cls-1" x="4" y="21" width="1" height="1" transform="translate(9 43) rotate(180)"/>
  <rect class="cls-1" x="3" y="21" width="1" height="1" transform="translate(7 43) rotate(180)"/>
  <rect class="cls-1" x="3" y="20" width="1" height="1" transform="translate(7 41) rotate(180)"/>
  <rect class="cls-1" x="2" y="20" width="1" height="1" transform="translate(5 41) rotate(180)"/>
  <rect class="cls-1" x="2" y="19" width="1" height="1" transform="translate(5 39) rotate(180)"/>
  <rect class="cls-1" x="2" y="18" width="1" height="1" transform="translate(5 37) rotate(180)"/>
  <rect class="cls-1" x="1" y="18" width="1" height="1" transform="translate(3 37) rotate(180)"/>
  <rect class="cls-1" x="1" y="17" width="1" height="1" transform="translate(3 35) rotate(180)"/>
  <rect class="cls-1" x="1" y="16" width="1" height="1" transform="translate(3 33) rotate(180)"/>
  <rect class="cls-1" y="16" width="1" height="1" transform="translate(1 33) rotate(180)"/>
  <rect class="cls-1" y="15" width="1" height="1" transform="translate(1 31) rotate(180)"/>
  <rect class="cls-1" y="14" width="1" height="1" transform="translate(1 29) rotate(180)"/>
  <rect class="cls-1" y="13" width="1" height="1" transform="translate(1 27) rotate(180)"/>
  <rect class="cls-1" x="25" y="13" width="1" height="1" transform="translate(39 -12) rotate(90)"/>
  <rect class="cls-1" x="25" y="14" width="1" height="1" transform="translate(40 -11) rotate(90)"/>
  <rect class="cls-1" x="25" y="15" width="1" height="1" transform="translate(41 -10) rotate(90)"/>
  <rect class="cls-1" x="25" y="16" width="1" height="1" transform="translate(42 -9) rotate(90)"/>
  <rect class="cls-1" x="24" y="16" width="1" height="1" transform="translate(41 -8) rotate(90)"/>
  <rect class="cls-1" x="24" y="17" width="1" height="1" transform="translate(42 -7) rotate(90)"/>
  <rect class="cls-1" x="24" y="18" width="1" height="1" transform="translate(43 -6) rotate(90)"/>
  <rect class="cls-1" x="23" y="18" width="1" height="1" transform="translate(42 -5) rotate(90)"/>
  <rect class="cls-1" x="23" y="19" width="1" height="1" transform="translate(43 -4) rotate(90)"/>
  <rect class="cls-1" x="23" y="20" width="1" height="1" transform="translate(44 -3) rotate(90)"/>
  <rect class="cls-1" x="22" y="20" width="1" height="1" transform="translate(43 -2) rotate(90)"/>
  <rect class="cls-1" x="22" y="21" width="1" height="1" transform="translate(44 -1) rotate(90)"/>
  <rect class="cls-1" x="21" y="21" width="1" height="1" transform="translate(43) rotate(90)"/>
  <rect class="cls-1" x="21" y="22" width="1" height="1" transform="translate(44 1) rotate(90)"/>
  <rect class="cls-1" x="20" y="22" width="1" height="1" transform="translate(43 2) rotate(90)"/>
  <rect class="cls-1" x="20" y="23" width="1" height="1" transform="translate(44 3) rotate(90)"/>
  <rect class="cls-1" x="19" y="23" width="1" height="1" transform="translate(43 4) rotate(90)"/>
  <rect class="cls-1" x="18" y="23" width="1" height="1" transform="translate(42 5) rotate(90)"/>
  <rect class="cls-1" x="18" y="24" width="1" height="1" transform="translate(43 6) rotate(90)"/>
  <rect class="cls-1" x="17" y="24" width="1" height="1" transform="translate(42 7) rotate(90)"/>
  <rect class="cls-1" x="16" y="24" width="1" height="1" transform="translate(41 8) rotate(90)"/>
  <rect class="cls-1" x="16" y="25" width="1" height="1" transform="translate(42 9) rotate(90)"/>
  <rect class="cls-1" x="15" y="25" width="1" height="1" transform="translate(41 10) rotate(90)"/>
  <rect class="cls-1" x="14" y="25" width="1" height="1" transform="translate(40 11) rotate(90)"/>
  <rect class="cls-1" x="13" y="25" width="1" height="1" transform="translate(39 12) rotate(90)"/>
  <rect class="cls-1" x="12" y="8" width="1" height="1"/>
  <rect class="cls-1" x="13" y="8" width="1" height="1"/>
  <rect class="cls-1" x="14" y="8" width="1" height="1"/>
  <rect class="cls-1" x="14" y="7" width="1" height="1"/>
  <rect class="cls-1" x="13" y="7" width="1" height="1"/>
  <rect class="cls-1" x="12" y="7" width="1" height="1"/>
  <rect class="cls-1" x="12" y="6" width="1" height="1"/>
  <rect class="cls-1" x="13" y="6" width="1" height="1"/>
  <rect class="cls-1" x="13" y="7" width="1" height="1"/>
  <rect class="cls-1" x="12" y="7" width="1" height="1"/>
  <rect class="cls-1" x="11" y="7" width="1" height="1"/>
  <rect class="cls-1" x="11" y="8" width="1" height="1"/>
  <rect class="cls-1" x="11" y="9" width="1" height="1"/>
  <rect class="cls-1" x="12" y="9" width="1" height="1"/>
  <rect class="cls-1" x="13" y="9" width="1" height="1"/>
  <rect class="cls-1" x="14" y="9" width="1" height="1"/>
  <rect class="cls-1" x="14" y="10" width="1" height="1"/>
  <rect class="cls-1" x="13" y="10" width="1" height="1"/>
  <rect class="cls-1" x="12" y="10" width="1" height="1"/>
  <rect class="cls-1" x="11" y="10" width="1" height="1"/>
  <rect class="cls-1" x="12" y="10" width="1" height="1"/>
  <rect class="cls-1" x="12" y="11" width="1" height="1"/>
  <rect class="cls-1" x="13" y="11" width="1" height="1"/>
  <rect class="cls-1" x="13" y="12" width="1" height="1"/>
  <rect class="cls-1" x="12" y="12" width="1" height="1"/>
  <rect class="cls-1" x="11" y="12" width="1" height="1"/>
  <rect class="cls-1" x="10" y="12" width="1" height="1"/>
  <rect class="cls-1" x="9" y="12" width="1" height="1"/>
  <rect class="cls-1" x="8" y="12" width="1" height="1"/>
  <rect class="cls-1" x="8" y="13" width="1" height="1"/>
  <rect class="cls-1" x="7" y="13" width="1" height="1"/>
  <rect class="cls-1" x="7" y="14" width="1" height="1"/>
  <rect class="cls-1" x="7" y="15" width="1" height="1"/>
  <rect class="cls-1" x="8" y="15" width="1" height="1"/>
  <rect class="cls-1" x="9" y="15" width="1" height="1"/>
  <rect class="cls-1" x="10" y="15" width="1" height="1"/>
  <rect class="cls-1" x="11" y="15" width="1" height="1"/>
  <rect class="cls-1" x="12" y="15" width="1" height="1"/>
  <rect class="cls-1" x="13" y="15" width="1" height="1"/>
  <rect class="cls-1" x="14" y="15" width="1" height="1"/>
  <rect class="cls-1" x="15" y="15" width="1" height="1"/>
  <rect class="cls-1" x="16" y="15" width="1" height="1"/>
  <rect class="cls-1" x="17" y="15" width="1" height="1"/>
  <rect class="cls-1" x="18" y="15" width="1" height="1"/>
  <rect class="cls-1" x="18" y="14" width="1" height="1"/>
  <rect class="cls-1" x="18" y="13" width="1" height="1"/>
  <rect class="cls-1" x="17" y="13" width="1" height="1"/>
  <rect class="cls-1" x="17" y="12" width="1" height="1"/>
  <rect class="cls-1" x="16" y="12" width="1" height="1"/>
  <rect class="cls-1" x="15" y="12" width="1" height="1"/>
  <rect class="cls-1" x="14" y="12" width="1" height="1"/>
  <rect class="cls-1" x="14" y="13" width="1" height="1"/>
  <rect class="cls-1" x="15" y="13" width="1" height="1"/>
  <rect class="cls-1" x="16" y="13" width="1" height="1"/>
  <rect class="cls-1" x="16" y="14" width="1" height="1"/>
  <rect class="cls-1" x="17" y="14" width="1" height="1"/>
  <rect class="cls-1" x="16" y="14" width="1" height="1"/>
  <rect class="cls-1" x="15" y="14" width="1" height="1"/>
  <rect class="cls-1" x="14" y="14" width="1" height="1"/>
  <rect class="cls-1" x="13" y="14" width="1" height="1"/>
  <rect class="cls-1" x="12" y="14" width="1" height="1"/>
  <rect class="cls-1" x="11" y="14" width="1" height="1"/>
  <rect class="cls-1" x="10" y="14" width="1" height="1"/>
  <rect class="cls-1" x="9" y="14" width="1" height="1"/>
  <rect class="cls-1" x="8" y="14" width="1" height="1"/>
  <rect class="cls-1" x="8" y="13" width="1" height="1"/>
  <rect class="cls-1" x="9" y="13" width="1" height="1"/>
  <rect class="cls-1" x="10" y="13" width="1" height="1"/>
  <rect class="cls-1" x="11" y="13" width="1" height="1"/>
  <rect class="cls-1" x="12" y="13" width="1" height="1"/>
  <rect class="cls-1" x="13" y="13" width="1" height="1"/>
  <rect class="cls-1" x="13" y="14" width="1" height="1"/>
  <rect class="cls-1" x="13" y="15" width="1" height="1"/>
  <rect class="cls-1" x="13" y="16" width="1" height="1"/>
  <rect class="cls-1" x="14" y="16" width="1" height="1"/>
  <rect class="cls-1" x="15" y="16" width="1" height="1"/>
  <rect class="cls-1" x="16" y="16" width="1" height="1"/>
  <rect class="cls-1" x="17" y="16" width="1" height="1"/>
  <rect class="cls-1" x="18" y="16" width="1" height="1"/>
  <rect class="cls-1" x="17" y="16" width="1" height="1"/>
  <rect class="cls-1" x="16" y="16" width="1" height="1"/>
  <rect class="cls-1" x="15" y="16" width="1" height="1"/>
  <rect class="cls-1" x="14" y="16" width="1" height="1"/>
  <rect class="cls-1" x="13" y="16" width="1" height="1"/>
  <rect class="cls-1" x="12" y="16" width="1" height="1"/>
  <rect class="cls-1" x="11" y="16" width="1" height="1"/>
  <rect class="cls-1" x="10" y="16" width="1" height="1"/>
  <rect class="cls-1" x="9" y="16" width="1" height="1"/>
  <rect class="cls-1" x="8" y="16" width="1" height="1"/>
  <rect class="cls-1" x="7" y="16" width="1" height="1"/>
  <rect class="cls-1" x="7" y="17" width="1" height="1"/>
  <rect class="cls-1" x="8" y="17" width="1" height="1"/>
  <rect class="cls-1" x="9" y="17" width="1" height="1"/>
  <rect class="cls-1" x="10" y="17" width="1" height="1"/>
  <rect class="cls-1" x="11" y="17" width="1" height="1"/>
  <rect class="cls-1" x="12" y="17" width="1" height="1"/>
  <rect class="cls-1" x="13" y="17" width="1" height="1"/>
  <rect class="cls-1" x="14" y="17" width="1" height="1"/>
  <rect class="cls-1" x="15" y="17" width="1" height="1"/>
  <rect class="cls-1" x="16" y="17" width="1" height="1"/>
  <rect class="cls-1" x="17" y="17" width="1" height="1"/>
  <rect class="cls-1" x="18" y="17" width="1" height="1"/>
  <rect class="cls-1" x="19" y="17" width="1" height="1"/>
  <rect class="cls-1" x="19" y="16" width="1" height="1"/>
  <rect class="cls-1" x="19" y="15" width="1" height="1"/>
  <rect class="cls-1" x="18" y="15" width="1" height="1"/>
  <rect class="cls-1" x="17" y="15" width="1" height="1"/>
  <rect class="cls-1" x="16" y="15" width="1" height="1"/>
  <rect class="cls-1" x="15" y="15" width="1" height="1"/>
  <rect class="cls-1" x="14" y="15" width="1" height="1"/>
  <rect class="cls-1" x="13" y="15" width="1" height="1"/>
  <rect class="cls-1" x="12" y="15" width="1" height="1"/>
  <rect class="cls-1" x="11" y="15" width="1" height="1"/>
  <rect class="cls-1" x="10" y="15" width="1" height="1"/>
  <rect class="cls-1" x="9" y="15" width="1" height="1"/>
  <rect class="cls-1" x="8" y="15" width="1" height="1"/>
  <rect class="cls-1" x="7" y="15" width="1" height="1"/>
  <rect class="cls-1" x="6" y="15" width="1" height="1"/>
  <rect class="cls-1" x="6" y="16" width="1" height="1"/>
  <rect class="cls-1" x="6" y="17" width="1" height="1"/>
  <rect class="cls-1" x="6" y="16" width="1" height="1"/>
  <rect class="cls-1" x="7" y="16" width="1" height="1"/>
  <rect class="cls-1" x="8" y="16" width="1" height="1"/>
  <rect class="cls-1" x="9" y="16" width="1" height="1"/>
  <rect class="cls-1" x="10" y="16" width="1" height="1"/>
  <rect class="cls-1" x="10" y="15" width="1" height="1"/>
  <rect class="cls-1" x="10" y="14" width="1" height="1"/>
  <rect class="cls-1" x="10" y="13" width="1" height="1"/>
  <rect class="cls-1" x="10" y="12" width="1" height="1"/>
  <rect class="cls-1" x="11" y="12" width="1" height="1"/>
  <rect class="cls-1" x="11" y="11" width="1" height="1"/>
  <rect class="cls-1" x="12" y="11" width="1" height="1"/>
  <rect class="cls-1" x="13" y="11" width="1" height="1"/>
  <rect class="cls-1" x="14" y="11" width="1" height="1"/>
  <rect class="cls-1" x="14" y="12" width="1" height="1"/>
  <rect class="cls-1" x="14" y="11" width="1" height="1"/>
  <rect class="cls-1" x="14" y="10" width="1" height="1"/>
  <rect class="cls-1" x="13" y="10" width="1" height="1"/>
  <rect class="cls-1" x="12" y="10" width="1" height="1"/>
  <rect class="cls-1" x="12" y="9" width="1" height="1"/>
  <rect class="cls-1" x="11" y="9" width="1" height="1"/>
  <rect class="cls-1" x="10" y="9" width="1" height="1"/>
  <rect class="cls-1" x="10" y="8" width="1" height="1"/>
  <rect class="cls-1" x="11" y="8" width="1" height="1"/>
  <rect class="cls-1" x="12" y="8" width="1" height="1"/>
  <rect class="cls-1" x="13" y="8" width="1" height="1"/>
  <rect class="cls-1" x="14" y="8" width="1" height="1"/>
  <rect class="cls-1" x="15" y="8" width="1" height="1"/>
  <rect class="cls-1" x="15" y="9" width="1" height="1"/>
  <rect class="cls-1" x="15" y="10" width="1" height="1"/>
  <rect class="cls-1" x="14" y="10" width="1" height="1"/>
  <rect class="cls-1" x="13" y="10" width="1" height="1"/>
  <rect class="cls-1" x="12" y="10" width="1" height="1"/>
  <rect class="cls-1" x="11" y="10" width="1" height="1"/>
  <rect class="cls-1" x="10" y="10" width="1" height="1"/>
</svg>`;

  
    // Array to store the points
  const points = [
    { x: 150, y: 75 },
    { x: 75, y: 85 },
    { x: 225, y: 65 },
    { x: 250, y: 75 },
    { x: 55, y: 120 },
    { x: 95, y: 120 },
    { x: 140, y: 110 },
    { x: 200, y: 100 },
    { x: 210, y: 100 },
    { x: 80, y: 200 },
    { x: 175, y: 200 },
    { x: 160, y: 210 },
    { x: 185, y: 230 },
    { x: 200, y: 250 }
  ];

    // Desired size for the SVG icons
    const iconWidth = 30; // New width for the SVG icons
  const iconHeight = 30; // New height for the SVG icons

  onMount(() => {
    ctx = canvas.getContext("2d");

    // Create an Image object for the SVG
    const img = new Image();
    img.src = `data:image/svg+xml;base64,${btoa(svgIcon)}`;

    // Once the image is loaded, draw it on the canvas
    img.onload = () => {
      drawIcons(img);
    };

    // Redraw icons on window resize
    window.addEventListener("resize", () => drawIcons(img));

    // Cleanup event listener on destroy
    onDestroy(() => {
      window.removeEventListener("resize", () => drawIcons(img));
    });
  });

  function drawIcons(img) {
    // Clear the canvas before redrawing
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    points.forEach(point => {
      // Draw the SVG icon at each point with the new width and height
      ctx.drawImage(img, point.x - iconWidth / 2, point.y - iconHeight / 2, iconWidth, iconHeight);
    });
  }
</script>

<canvas bind:this={canvas} width="300" height="300"></canvas>

<style>
  canvas {
    background-color: white;
    display: block;
  }
</style>