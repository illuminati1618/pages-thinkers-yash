---
layout: base
title: Lesson Plan --> Can you play rock, paper, scissors shoot with us?
permalink: /gamify/rock_paper_scissors_shoot
---

<div class="rps-lesson">
  <div class="container">
    <h1>Rock Paper Scissors Console Learning</h1>
    <p class="subtitle">
      A hands-on introduction to browser developer tools through interactive gameplay!!
    </p>

    <div class="play-instructions">
      Try the game now! Open your browser's developer tools (F12 or right-click → Inspect), 
      go to the Console tab, and type: playRPS("rock")
    </div>

    <div class="game-buttons">
      <button onclick="playRPS('rock')">Rock</button>
      <button onclick="playRPS('paper')">Paper</button>
      <button onclick="playRPS('scissors')">Scissors</button>
    </div>

    <h2>What is Browser Console Development?</h2>
    <p>
      Browser developer tools are built-in debugging environments that let you interact with web pages behind the scenes. 
      The <strong>Console</strong> is where developers test JavaScript code, debug programs, and explore how web applications work in real-time.
    </p>

    <h3>Understanding the Developer Tools Interface</h3>
    <div class="section-highlight">
      <h4>Console Tab Features:</h4>
      <ul>
        <li><strong>Interactive JavaScript Environment:</strong> Type commands and see immediate results</li>
        <li><strong>Function Testing:</strong> Call functions directly without needing buttons or forms</li>
        <li><strong>Output Tracking:</strong> View console.log() statements and error messages</li>
        <li><strong>Live Code Execution:</strong> Test code changes without modifying source files</li>
      </ul>

      <h4>Inspect Element Features:</h4>
      <ul>
        <li><strong>HTML Structure:</strong> See the actual markup that creates the webpage</li>
        <li><strong>CSS Styling:</strong> View and modify styles applied to elements</li>
        <li><strong>Network Activity:</strong> Monitor requests and responses between browser and server</li>
      </ul>
    </div>

    <h2>The Rock Paper Scissors Console Game</h2>
    <p>
      This interactive lesson teaches console navigation through a familiar game. Instead of clicking buttons, you'll execute JavaScript functions directly in the console.
    </p>

    <div class="section-highlight">
      <h3>Game Setup Process</h3>
      <h4>Step-by-Step Instructions:</h4>
      <ol>
        <li>
          <strong>Access Developer Tools</strong>
          <ul>
            <li>Right-click anywhere on this page</li>
            <li>Select "Inspect" or "Inspect Element" from the menu</li>
            <li>
              Alternative: Use keyboard shortcuts
              <ul>
                <li>Windows/Linux: Ctrl + Shift + I or F12</li>
                <li>Mac: Cmd + Option + I</li>
              </ul>
            </li>
          </ul>
        </li>
        <li>
          <strong>Navigate to Console</strong>
          <ul>
            <li>Click "Console" to switch to the interactive environment</li>
            <li>You should see a command prompt (usually > symbol)</li>
          </ul>
        </li>
        <li>
          <strong>Execute Game Commands</strong>
          <ul>
            <li>Type exactly: playRPS("rock") and press Enter</li>
            <li>Try other choices: playRPS("paper") or playRPS("scissors")</li>
            <li>Watch the console display your results in real-time</li>
          </ul>
        </li>
      </ol>

      <h4>Sample Console Interaction</h4>
      <div class="console-example" style="background:#cce7ff; color:#0f0;">
        > playRPS("rock")  
        You chose: ROCK  
        Computer chose: SCISSORS  
        Result: You Win!  

        > playRPS("paper")  
        You chose: PAPER  
        Computer chose: PAPER  
        Result: Tie!  

        > playRPS("scissors")  
        You chose: SCISSORS  
        Computer chose: ROCK  
        Result: You Lose!
      </div>
    </div>

    <h2>Learning Workflow (Flow Chart)</h2>
    <p>The following visual flow represents how students progress through console skills:</p>

    <div style="display:flex; flex-direction:column; align-items:center; gap:1.5rem; margin:2rem 0; font-family:sans-serif;">
      <!-- Phase 1 -->
      <div style="padding:1rem 1.5rem; border:2px solid #1f2937; border-radius:8px; max-width:500px; text-align:left; background:#003c00;">
        <h3>Phase 1: Basic Console Navigation</h3>
        <ul>
          <li>Open developer tools confidently</li>
          <li>Navigate between Console and Elements tabs</li>
          <li>Execute simple JavaScript commands</li>
          <li>Read and interpret console output</li>
        </ul>
      </div>

      <!-- Arrow -->
      <svg width="48" height="48" viewBox="0 0 48 48" aria-hidden="true">
        <line x1="24" y1="8" x2="24" y2="40" stroke="#817114ff" stroke-width="8" stroke-linecap="round"/>
        <polyline points="12,32 24,44 36,32" fill="none" stroke="#51491aff" stroke-width="8" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>

      <!-- Phase 2 -->
      <div style="padding:1rem 1.5rem; border:2px solid #1f2937; border-radius:8px; max-width:500px; text-align:left; background:#003c00;">
        <h3>Phase 2: Function Interaction</h3>
        <ul>
          <li>Call functions with different parameters</li>
          <li>Understand how arguments affect results</li>
          <li>Recognize patterns in program behavior</li>
          <li>Predict outcomes based on code logic</li>
        </ul>
      </div>

      <!-- Arrow -->
      <svg width="48" height="48" viewBox="0 0 48 48" aria-hidden="true">
        <line x1="24" y1="8" x2="24" y2="40" stroke="#4b4002ff" stroke-width="8" stroke-linecap="round"/>
        <polyline points="12,32 24,44 36,32" fill="none" stroke="#bfa100" stroke-width="8" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>

      <!-- Phase 3 -->
      <div style="padding:1rem 1.5rem; border:2px solid #1f2937; border-radius:8px; max-width:500px; text-align:left; background:#003c00;">
        <h3>Phase 3: Code Analysis</h3>
        <ul>
          <li>Read JavaScript code and understand its purpose</li>
          <li>Identify key programming concepts (variables, functions, conditionals)</li>
          <li>Trace execution flow from input to output</li>
          <li>Connect console results to underlying code logic</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<script>
  // Rock Paper Scissors Console Game
  window.playRPS = function(playerChoice) {
    if (!playerChoice || typeof playerChoice !== 'string') {
      console.error('Please provide a valid choice: "rock", "paper", or "scissors"');
      return;
    }

    playerChoice = playerChoice.toLowerCase();
    const choices = ["rock", "paper", "scissors"];

    if (!choices.includes(playerChoice)) {
      console.error('Invalid choice! Please use "rock", "paper", or "scissors"');
      return;
    }

    const computerChoice = choices[Math.floor(Math.random() * choices.length)];
    let resultText;

    if (playerChoice === computerChoice) {
      resultText = "Tie!";
    } else if (
      (playerChoice === "rock" && computerChoice === "scissors") ||
      (playerChoice === "paper" && computerChoice === "rock") ||
      (playerChoice === "scissors" && computerChoice === "paper")
    ) {
      resultText = "You Win!";
    } else {
      resultText = "You Lose!";
    }

    console.log(`%cYou chose: ${playerChoice.toUpperCase()}`, 'color: #3b82f6; font-weight: bold;');
    console.log(`%cComputer chose: ${computerChoice.toUpperCase()}`, 'color: #ef4444; font-weight: bold;');
    console.log(`%c${resultText}`, 'color: #10b981; font-size: 16px; font-weight: bold;');
    console.log('---');

    return { player: playerChoice, computer: computerChoice, result: resultText };
  };

  console.log('%cRock Paper Scissors Console Game Ready!', 'color: #ffd700; font-size: 18px; font-weight: bold;');
  console.log('%cTry: playRPS("rock"), playRPS("paper"), or playRPS("scissors")', 'color: #6366f1; font-weight: bold;');
</script>

## Moving Paper Demo

<div id="gameArea" style="position:relative; width:600px; height:400px; border:1px solid #333; overflow:hidden; margin:20px auto;">
  <img id="paperImage" src="{{site.baseurl}}/images/gamify/scissors.jpeg" 
       alt="Paper" 
       style="position:absolute; width:80px; height:80px;">
</div>

<button id="stopBtn" style="display:block; margin:10px auto; padding:10px 20px; font-size:16px;">Stop Motion</button>

<script>
class MovingPaper {
  constructor(imageId, containerId) {
    this.image = document.getElementById(imageId);
    this.container = document.getElementById(containerId);
    this.interval = null;
  }

  startMotion() {
    this.interval = setInterval(() => {
      let maxX = this.container.offsetWidth - this.image.offsetWidth;
      let maxY = this.container.offsetHeight - this.image.offsetHeight;

      let newX = Math.floor(Math.random() * maxX);
      let newY = Math.floor(Math.random() * maxY);

      this.image.style.left = newX + "px";
      this.image.style.top = newY + "px";
    }, 800);
  }

  stopMotion() {
    clearInterval(this.interval);
  }
}

// create the paper object
const paper = new MovingPaper("paperImage", "gameArea");
paper.startMotion();

// button event
document.getElementById("stopBtn").addEventListener("click", () => {
  paper.stopMotion();
});
</script>

<div id="oopExplanation" style="max-width:700px; margin:30px auto; padding:20px; background:#f0f8ff; border-radius:10px; border:1px solid #ccc;">
  <h2>How the OOP Code Works</h2>
  <p>
    The JavaScript code is written using <b>Object-Oriented Programming (OOP)</b>. Instead of writing separate 
    functions scattered across the script, we bundle everything related to the moving paper into a single 
    <code>MovingPaper</code> class. This makes the code more organized and reusable.
  </p>

  <h3>Breaking it down:</h3>
  <ul>
    <li>
      <b>Class Definition:</b>  
      <code>class MovingPaper {...}</code> creates a blueprint for paper objects. Any paper we create 
      from this class will automatically know how to move and stop.
    </li>
    <li>
      <b>Constructor:</b>  
      <code>constructor(imageId, containerId)</code> runs once when we make a new paper object.  
      - It grabs the paper image from the HTML using its ID.  
      - It also remembers the container (the box where the paper is allowed to move).  
      - Finally, it sets up a variable (<code>this.interval</code>) that will later control movement timing.
    </li>
    <li>
      <b><code>startMotion()</code>:</b>  
      - Uses <code>setInterval()</code> to repeat code every 800 milliseconds.  
      - Picks a random X and Y inside the container.  
      - Updates the paper’s CSS position so it “jumps” around.  
      - Keeps looping until stopped.
    </li>
    <li>
      <b><code>stopMotion()</code>:</b>  
      Calls <code>clearInterval()</code> to stop the timer so the paper freezes in place.
    </li>
  </ul>

  <h3>How we use the class:</h3>
  <p>
    At the bottom of the script, we create a new object with <code>const paper = new MovingPaper("paperImage", "gameArea");</code>.  
    This tells JavaScript: “Here’s a paper image inside the game area, make it move!”  
  </p>
  <p>
    Then, we immediately call <code>paper.startMotion()</code> to begin the random movement.  
    Finally, the "Stop Motion" button is connected to <code>paper.stopMotion()</code>, so when you click it, the paper freezes.
  </p>

  <h3>Why OOP is useful here:</h3>
  <p>
    If later we wanted to add multiple moving images (like Rock, Paper, and Scissors each moving), 
    we could just create more objects from the same <code>MovingPaper</code> class without rewriting all the code.  
    That’s the power of OOP — reusable, clean, and easy to scale.
  </p>
</div>
