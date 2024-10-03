<script>
    import { onMount, tick } from 'svelte';
    import defaultPerson from '$lib/assets/sillhoette.png';
  
    // Props
    export let name = "";
    export let facts = [];
    export let treeTop = [];
    export let treeMid = [];
    export let treeBottom = [];
    export let imageUrl = ""; // New prop for the person's image URL

    // State to manage modal visibility
    let isModalOpen = false;
  
    // Function to open the modal
    async function openModal() {
        if (isModalOpen === true ){return}
      isModalOpen = true;
      await tick();  // Wait for DOM updates
      drawLines();   // Draw lines after DOM is fully updated
    }
  
    // Function to close the modal
    function handleClose() {
      isModalOpen = false;
      removeLines();  // Remove lines when closing the modal
    }
  
    // Function to draw lines
    function drawLines() {
      const dots = document.querySelectorAll('.dot');
      const dotXl = document.querySelector('.dot-xl');
      const infoModal = document.querySelector('.info-modal');
  
      if (!infoModal || !dotXl) return; // Check for null
  
      dots.forEach(dot => {
        const line = document.createElement('div');
        line.classList.add('line');
  
        const dotRect = dot.getBoundingClientRect();
        const dotXlRect = dotXl.getBoundingClientRect();
        const infoModalRect = infoModal.getBoundingClientRect();
  
        const x1 = dotRect.left + dotRect.width / 2 - infoModalRect.left;
        const y1 = dotRect.top + dotRect.height / 2 - infoModalRect.top;
        const x2 = dotXlRect.left + dotXlRect.width / 2 - infoModalRect.left;
        const y2 = dotXlRect.top + dotXlRect.height / 2 - infoModalRect.top;
  
        const length = Math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2);
        const angle = Math.atan2(y2 - y1, x2 - x1) * (180 / Math.PI);
  
        line.style.width = `${length}px`;
        line.style.transform = `rotate(${angle}deg)`;
        line.style.position = 'absolute';
        line.style.top = `${y1}px`;
        line.style.left = `${x1}px`;
        line.style.backgroundColor = 'red'; // Changed to red
        line.style.height = '2px';
        line.style.transformOrigin = '0 0';
  
        infoModal.appendChild(line);
      });
    }
  
    // Function to remove lines
    function removeLines() {
      const lines = document.querySelectorAll('.line');
      lines.forEach(line => line.remove());
    }
  
    //** Ensure lines are drawn after the modal is visible and DOM is updated
    //onMount(async () => {
    //  if (isModalOpen) {
    //    await tick(); 
    //    drawLines();  
    //  }
    //});
    
  </script>
  
  <!-- Wrapping the component content -->
  <span on:click={openModal} style="cursor: pointer;">
    <slot></slot>
  </span>
  
  <!-- Modal with dynamic content -->
  {#if isModalOpen}
    <div class="info-modal">
      <!-- Title Bar -->
      <button on:click={handleClose} class="close-button">X</button>
      
      <!-- Tree Top -->
        <div class="person-info">
            <div class="image-container">
                <img src={imageUrl || defaultPerson} alt="person icon" class={imageUrl ? 'circular' : ''}/>
            </div>
            <div class="person-info-text">
                <span class="person-name">{name}</span>
                <ul>
                    {#each facts as fact}
                    <li>{fact}</li>
                    {/each}
                </ul>
            </div>

        </div>
      <div class="tree-top">
        {#each treeTop as person}
          <div class="person">
            {#if person.link}
              <a href={person.link}>{person.name}</a>
            {:else}
              <span>{person.name}</span>
            {/if}
            <div class="dot"></div>
          </div>
        {/each}
      </div>
  
      <!-- Tree Mid -->
      <div class="tree-mid">
        {#each treeMid as person}
          <div class="person">
            <div class={person.main !== true ? 'dot' : 'dot-xl'}></div>
            {#if person.link}
              <a on:click={handleClose} href={person.link}>{person.name}</a>
            {:else}
              <span>{person.name}</span>
            {/if}
          </div>
        {/each}
      </div>
  
      <!-- Tree Bottom -->
      <div class="tree-bottom">
        {#each treeBottom as person}
          <div class="person">
            {#if person.link}
              <a href={person.link}>{person.name}</a>
            {:else}
              <span>{person.name}</span>
            {/if}
            <div class="dot"></div>
          </div>
        {/each}
      </div>
    </div>
  {/if}
  
  <style>
    /* Windows 95 Style */

    .person-name {
        font-size: 20px;
        color: black;
    }

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    img.circular {
        border-radius: 50%;
    }

    .image-container {
        width: 75px;
        height: 75px;
        overflow: hidden;
        border-radius: 50%;
    }

    ul {
        color: black;
        margin-top: 0;
        padding-left: 20px;
        font-family: Arial, Helvetica, sans-serif;
    }

    .person-info{
        display: flex;
        justify-content: center;
        gap: 20px;
        max-width: 100%;
        width: max-content;
    }

    .person-info-text{
        width: 80%;
    }

    body {
      background-color: #c0c0c0; /* Light gray background */
      font-family: Arial, Helvetica, sans-serif; /* Windows 95 font */
    }
  
    .dot {
      background-color: red; /* Changed to red */
      width: 10px;
      height: 10px;
      border-radius: 50%;
    }
  
    .dot-xl {
      background-color: red; /* Changed to red */
      width: 15px;
      height: 15px;
      border-radius: 50%;
    }
  
    .person {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      font-size: 0.9rem;
      color: black;
    }
  
    .info-modal {
      background-color: white; /* Slightly darker gray for the modal background */
      display: flex;
      flex-direction: column;
      gap: 20px;
      position: absolute;
      padding: 30px;
      width: 70%;
      right: 15%;
      z-index: 100;
      border-radius: 20px;
    }
  
    .title-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 4px;
      box-shadow: inset 1px 1px 0 #ffffff, inset -1px -1px 0 #000000; /* Beveled effect for title bar */
      height: 24px;
    }
  
    .title {
      font-size: 1rem;
      margin-left: 4px;
      color: white;
    }
  
    .close-button {
      background-color: #e4e4e4; /* Match modal background */
      border: none;
      background-color: red;
      border-radius: 5px;
      color: white;
      font-size: 1rem;
      cursor: pointer;
      padding: 2 8px;
      margin-right: 4px;
      font-family: Arial, Helvetica, sans-serif;
      width: 40px;
    }
  
    .close-button:hover {
      background-color: darkred; /* Darker gray on hover */
      cursor: pointer;
    }
  
    .tree-top, .tree-mid, .tree-bottom {
      display: flex;
      justify-content: center;
      gap: 20px;
    }
  
    .line {
      position: absolute;
      height: 2px;
      background-color: red; /* Changed to red */
      transform-origin: 0 0;
    }
  
    a, span {
      font-family: Arial, Helvetica, sans-serif;
    }
  
    a:hover {
      text-decoration: underline;
    }
  
    span {
      cursor: default;
    }
  
    .highlight {
      background-color: #d3d3d3; /* Lighter gray for highlights */
      color: black;
      padding: 2px 4px;
      font-family: Arial, Helvetica, sans-serif;
    }
  </style>
