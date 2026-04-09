---
layout: page
title: Fun Kids Games 🎮
permalink: /games/
---

<style>
  .game-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 20px;
    padding: 20px;
  }
  .game-card {
    background: #FFEB3B; /* Bright Yellow */
    border: 5px solid #FF9800; /* Orange Border */
    border-radius: 20px;
    padding: 15px;
    text-align: center;
    transition: transform 0.2s;
    cursor: pointer;
  }
  .game-card:hover {
    transform: scale(1.05) rotate(2deg);
  }
  .game-card h3 { color: #E91E63; margin-top: 10px; }
</style>

<div class="game-container">
  <div class="game-card">
    <img src="https://via.placeholder.com/150" style="border-radius: 15px;">
    <h3>Math Quiz</h3>
    <p>Fun with numbers!</p>
    <a href="/games/math-quiz" class="btn">PLAY NOW</a>
  </div>

  <div class="game-card" style="background: #90CAF9; border-color: #2196F3;">
    <img src="https://via.placeholder.com/150" style="border-radius: 15px;">
    <h3>Coloring Lab</h3>
    <p>Paint the world!</p>
    <a href="/games/coloring" class="btn">PLAY NOW</a>
  </div>
</div>
