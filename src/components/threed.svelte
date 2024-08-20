<script>
    import { onMount } from "svelte";
    import * as THREE from "three";
  
    let scene, camera, renderer;
    let elements = {};
  
    // Initialize scene and camera
    onMount(() => {
      // Create the scene
      scene = new THREE.Scene();
  
      // Create the camera
      camera = new THREE.PerspectiveCamera(
        75,
        window.innerWidth / window.innerHeight,
        0.1,
        1000
      );
      camera.position.z = 50;
  
      // Create the renderer
      renderer = new THREE.WebGLRenderer();
      renderer.setSize(window.innerWidth, window.innerHeight);
      document.body.appendChild(renderer.domElement);
  
      // Add some elements to the scene
      createElements();
  
      // Start the animation loop
      animate();
    });
  
    function createElements() {
      // Example elements (spheres) added to the scene
      const geometry = new THREE.SphereGeometry(1, 32, 32);
      const material = new THREE.MeshBasicMaterial({ color: 0xffffff });
  
      const names = ["Alice", "Bob", "Charlie"];
      names.forEach((name, index) => {
        const sphere = new THREE.Mesh(geometry, material);
        sphere.position.set(index * 10 - 10, 0, 0); // Positioning elements in a line
        scene.add(sphere);
        elements[name] = sphere; // Store reference to the element by name
      });
    }
  
    function animate() {
      requestAnimationFrame(animate);
      renderer.render(scene, camera);
    }
  
    function moveToName(name) {
      if (elements[name]) {
        const target = elements[name];
        const targetPosition = target.position;
  
        // Move and zoom the camera
        camera.position.x = targetPosition.x;
        camera.position.y = targetPosition.y;
        camera.position.z = 10; // Zoom in closer
      }
    }
  </script>
  
  <div>
    <button on:click={() => moveToName("Alice")}>Focus on Alice</button>
    <button on:click={() => moveToName("Bob")}>Focus on Bob</button>
    <button on:click={() => moveToName("Charlie")}>Focus on Charlie</button>
  </div>
  
  <style>
    canvas {
      display: block;
    }
  
    div {
      position: absolute;
      top: 10px;
      left: 10px;
    }
  
    button {
      margin: 5px;
    }
  </style>
  