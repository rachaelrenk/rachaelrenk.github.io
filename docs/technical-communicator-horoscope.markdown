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
    {
      text: "Stop thinking that willpower comes from confidence. Your track record proves otherwise. You've outlasted every crisis not because you felt ready, but because you refused to break. Remember that when today's challenges make you doubt yourself.",
      source: "Co-Star"
    }
    {
      text: "You stand at the threshold of ancient wisdom today. Your practical mind seeks meaning in structure, making this an ideal moment to connect with teachings that have stood time's test. What others see as your rigidity is actually your unique way of filtering timeless truths through a modern lens.",
      source: "Co-Star"
    }
    {
      text: "Your mind cuts through fog like a lighthouse beam. The current influence sharpens your already keen analytical skills, making this an ideal moment to tackle complex problems. The precision you bring to tasks isn't just about fixing flaws--it can be the foundation for bold creation.",
      source: "Co-Star"
    }
    {
      text: "You channel your ambition into communication, mental pursuits, and the exchange of ideas, and you show a kind of intellectual courage.",
      source: "The Pattern"
    }
    {
      text: "Your desire to break rules isn't rebellion--it's your m ind searching for new approaches to old problems.",
      source: "Co-Star"
    }
    {
      text: "Your mind works like a scalpel--precise, sharp, useful. Your analytical skills are heightened, making this an ideal time to solve problems that require attention to detail. What you mistake for perfectionism is actually your mind craving more complex challenges than your current routine offers.",
      source: "Co-Star" 
    }
    {
      text: "That small detail everyone else missed? It matters. Your suspicion isn't weakness--it's radar working perfectly. Turst it. Act accordingly.",
      source: "Co-Star"
    }
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