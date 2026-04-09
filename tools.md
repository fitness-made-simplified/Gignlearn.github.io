---
layout: page
title: Gigloo's Super Tools 🛠️
permalink: /tools/
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Fredoka+One&family=Quicksand:wght@500&display=swap');

  .tool-box {
    font-family: 'Quicksand', sans-serif;
    max-width: 800px;
    margin: 0 auto;
  }

  .tool-container {
    background: white;
    border-radius: 30px;
    padding: 40px;
    margin-bottom: 40px;
    text-align: center;
    box-shadow: 0 10px 20px rgba(0,0,0,0.05);
    transition: transform 0.3s ease;
  }

  .tool-container:hover {
    transform: translateY(-5px);
  }

  .tool-title {
    font-family: 'Fredoka One', cursive;
    font-size: 2rem;
    margin-bottom: 15px;
  }

  input {
    padding: 15px;
    border-radius: 15px;
    border: 3px solid #eee;
    width: 80%;
    max-width: 300px;
    font-size: 1.1rem;
    outline: none;
    transition: border-color 0.3s;
  }

  input:focus {
    border-color: #FF9800;
  }

  .kids-button {
    background: #FF9800;
    color: white;
    border: none;
    padding: 15px 35px;
    border-radius: 50px;
    font-size: 1.2rem;
    cursor: pointer;
    font-weight: bold;
    margin-top: 20px;
    box-shadow: 0 5px #E65100;
    transition: 0.2s;
  }

  .kids-button:active {
    transform: translateY(4px);
    box-shadow: 0 1px #E65100;
  }

  .result-text {
    margin-top: 25px;
    font-family: 'Fredoka One', cursive;
    color: #E91E63;
    min-height: 40px;
  }

  .tool-divider {
    border: none;
    height: 10px;
    background-image: radial-gradient(circle, #ccc 2px, transparent 2px);
    background-size: 20px 20px;
    margin: 40px 0;
  }
</style>

<div class="tool-box">

  <div class="tool-container" style="border: 5px solid #2196F3;">
    <h2 class="tool-title" style="color: #1565C0;">Tiger Name Generator 🐯</h2>
    <p>What would your name be in Gigloo's world?</p>
    
    <input type="text" id="userName" placeholder="Type your name here...">
    <br>
    <button class="kids-button" style="background: #2196F3; box-shadow: 0 5px #1976D2;" onclick="generateName()">Get Tiger Name! ✨</button>
    <h2 id="nameResult" class="result-text"></h2>
  </div>

  <hr class="tool-divider">

  <div class="tool-container" style="border: 5px solid #FF9800;">
    <h2 class="tool-title" style="color: #E65100;">Tiger Age Calculator 🐾</h2>
    <p>How many "Tiger Years" have you been roaring?</p>
    
    <input type="number" id="humanAge" placeholder="Enter your age">
    <br>
    <button class="kids-button" onclick="calcTigerAge()">Calculate! 🐯</button>
    <h2 id="tigerResult" class="result-text" style="color: #D84315;"></h2>
  </div>

  <hr class="tool-divider">

  <div class="tool-container" style="border: 5px solid #4CAF50;">
    <h2 class="tool-title" style="color: #2E7D32;">Gigloo's Goal Tracker ✅</h2>
    <p>Check off your big wins for today!</p>
    
    <div style="text-align: left; display: inline-block; font-size: 1.2rem;">
      <label><input type="checkbox" style="width: 20px;"> I brushed my teeth 🪥</label><br>
      <label><input type="checkbox" style="width: 20px;"> I read a story 📖</label><br>
      <label><input type="checkbox" style="width: 20px;"> I was kind to others 🧡</label><br>
      <label><input type="checkbox" style="width: 20px;"> I finished my homework ✍️</label>
    </div>
    <br>
    <button class="kids-button" style="background: #4CAF50; box-shadow: 0 5px #388E3C;" onclick="goalCelebrate()">I Finished! 🎉</button>
    <h2 id="goalResult" class="result-text" style="color: #2E7D32;"></h2>
  </div>

</div>

<script>
// Logic for Name Generator
function generateName() {
  const prefixes = ["Brave", "Happy", "Fast", "Smart", "Funny", "Cool", "Mighty", "Super"];
  const name = document.getElementById('userName').value;
  if(!name) { 
    document.getElementById('nameResult').innerText = "Please type a name first!";
    return; 
  }
  const randomPrefix = prefixes[Math.floor(Math.random() * prefixes.length)];
  document.getElementById('nameResult').innerText = `Your Tiger Name: ${randomPrefix} ${name}!`;
}

// Logic for Age Calculator
function calcTigerAge() {
  const age = document.getElementById('humanAge').value;
  if(!age || age <= 0) { 
    document.getElementById('tigerResult').innerText = "Enter a valid age!";
    return; 
  }
  const tigerAge = age * 7;
  document.getElementById('tigerResult').innerText = `You are ${tigerAge} Tiger Years old! ROAR!`;
}

// Logic for Goal Tracker
function goalCelebrate() {
  document.getElementById('goalResult').innerText = "Great job! Gigloo is proud of you! 🐯🏆";
}
</script>

