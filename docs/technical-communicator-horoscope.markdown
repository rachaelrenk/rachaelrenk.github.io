---
layout: page
title: Horoscope
permalink: /technical-communicator-horoscope/
order: 4
---

<div class="horoscope-container">
  <h2>Rachael's Technical Communicator Horoscope</h2>
  
  <div class="horoscope-card" id="horoscope-display">
    <!-- Horoscope will be injected here by JavaScript -->
  </div>
  
  <button class="refresh-horoscope" onclick="loadNewHoroscope()">✨ Get Another Reading</button>
</div>

<script>
  // Array of horoscopes
  const horoscopes = [
    {
      text: "You seek deep meaning and speak only what feels true. You also notice details others miss. This creates a powerful communication style that lends itself to solving complicated problems with passionate, well-researched solutions.",
      source: "Co-Star"
    },
    // Add more horoscopes here as objects with 'text' and 'source' properties
  ];

  // Function to get a random horoscope
  function getRandomHoroscope() {
    const randomIndex = Math.floor(Math.random() * horoscopes.length);
    return horoscopes[randomIndex];
  }

  // Function to display a horoscope
  function displayHoroscope(horoscope) {
    const container = document.getElementById('horoscope-display');
    container.innerHTML = `
      <p class="horoscope-text">${horoscope.text}</p>
      <p class="horoscope-source">— ${horoscope.source}</p>
    `;
    
    // Add fade-in animation
    container.style.animation = 'none';
    setTimeout(() => {
      container.style.animation = 'fadeIn 0.5s ease-in';
    }, 10);
  }

  // Function to load a new horoscope
  function loadNewHoroscope() {
    const horoscope = getRandomHoroscope();
    displayHoroscope(horoscope);
  }

  // Load initial horoscope on page load
  document.addEventListener('DOMContentLoaded', function() {
    loadNewHoroscope();
  });
</script>

---

<div style="text-align: center; margin-top: 3rem;">
  <a href="/" style="font-size: 1.1rem;">← Back to portfolio</a>
</div>