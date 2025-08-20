---
layout: base
title: Lesson Plan--> Can you play rock, paper, scissors shoot with us?
permalink: /gamify/rock_paper_scissors_shoot
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rock Paper Scissors Console Learning</title>
    <style>
      /* Force light mode and prevent browser overrides */
          :root {
              color-scheme: only dark !important;
          }
          body, body * {
              color: #000000 !important;
          }
          /* Ensure high contrast */
          h1, h2, h3, h4, h5, h6 {
              color: #1f2937 !important;
          }
          p, li, span, div {
              color: #374151 !important;
          }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1e3a8a, #3730a3);
            color: #1f2937;
            margin: 0;
            padding: 20px;
            line-height: 1.6;
            min-height: 100vh;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: #ffffff;
            padding: 40px;
            border: 3px solid #ffd700;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        h1 {
            color: #1f2937;
            text-align: center;
            font-size: 2.5em;
            margin-bottom: 10px;
            border-bottom: 3px solid #ffd700;
            padding-bottom: 10px;
            font-weight: bold;
        }
        h2 {
            color: #1f2937;
            font-size: 1.8em;
            border-left: 4px solid #c06c84;
            padding-left: 15px;
            margin-top: 30px;
            font-weight: bold;
        }
        h3 {
            color: #1f2937;
            font-size: 1.4em;
            margin-top: 25px;
            font-weight: bold;
        }
        h4 {
            color: #1f2937;
            font-size: 1.2em;
            margin-top: 20px;
            font-weight: bold;
        }
        .subtitle {
            text-align: center;
            color: #4b5563;
            font-style: italic;
            font-size: 1.2em;
            margin-bottom: 30px;
        }
        .game-buttons {
            text-align: center;
            margin: 30px 0;
        }
        button {
            background: linear-gradient(45deg, #ffd700, #c06c84);
            color: #1f2937;
            border: none;
            padding: 15px 30px;
            margin: 0 10px;
            border-radius: 8px;
            font-size: 1.1em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }
        button:hover {
            background: linear-gradient(45deg, #c06c84, #6a4c93);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.3);
        }
        button:active {
            transform: translateY(-1px);
        }
        .console-example {
            background: #1a1a1a;
            color: #00ff41;
            padding: 20px;
            font-family: 'Courier New', monospace;
            margin: 20px 0;
            border: 2px solid #ffd700;
            border-radius: 8px;
            overflow-x: auto;
            font-size: 0.95em;
        }
        .code-block {
            background: #f8fafc;
            color: #1f2937;
            padding: 20px;
            font-family: 'Courier New', monospace;
            margin: 20px 0;
            border: 2px solid #c06c84;
            border-radius: 8px;
            overflow-x: auto;
            font-size: 0.9em;
            border-left: 4px solid #6a4c93;
        }
        .section-highlight {
            background: linear-gradient(135deg, rgba(255, 215, 0, 0.1), rgba(192, 108, 132, 0.1));
            padding: 25px;
            margin: 25px 0;
            border: 1px solid #c06c84;
            border-radius: 8px;
        }
        .phase-section {
            background: rgba(106, 76, 147, 0.1);
            padding: 20px;
            margin: 20px 0;
            border-left: 4px solid #6a4c93;
            border-radius: 5px;
        }
        ul, ol {
            margin: 15px 0;
            padding-left: 30px;
        }
        li {
            margin: 8px 0;
            color: #374151;
        }
        p {
            color: #374151;
            margin: 15px 0;
        }
        strong {
            color: #1f2937;
            font-weight: bold;
        }
        .success-indicators {
            background: rgba(255, 215, 0, 0.15);
            padding: 25px;
            margin: 30px 0;
            border: 2px solid #ffd700;
            border-radius: 8px;
        }
        .activities-section {
            background: rgba(192, 108, 132, 0.1);
            padding: 25px;
            margin: 25px 0;
            border: 1px solid #c06c84;
            border-radius: 8px;
        }
        .play-instructions {
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            color: #1f2937;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            font-weight: bold;
            margin: 20px 0;
            border: 2px solid #d97706;
        }
    </style>
</head>
<body>
<div class="container">
    <h1>Rock Paper Scissors Console Learning</h1>
    <p class="subtitle">A hands-on introduction to browser developer tools through interactive gameplay</p>

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
    <p>Browser developer tools are built-in debugging environments that let you interact with web pages behind the scenes. The <strong>Console</strong> is where developers test JavaScript code, debug programs, and explore how web applications work in real-time.</p>

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
    <p>This interactive lesson teaches console navigation through a familiar game. Instead of clicking buttons, you'll execute JavaScript functions directly in the console.</p>

    <div class="section-highlight">
        <h3>Game Setup Process</h3>
        <h4>Step-by-Step Instructions:</h4>
        <ol>
            <li>
                <strong>Access Developer Tools</strong>
                <ul>
                    <li>Right-click anywhere on this page</li>
                    <li>Select "Inspect" or "Inspect Element" from the menu</li>
                    <li>Alternative: Use keyboard shortcuts
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
                    <li>Try other choices: <code>playRPS("paper") or playRPS("scissors") </li>
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

    <div style="display:flex; flex-direction:column; align-items:center; gap:1rem; margin:2rem 0; font-family:sans-serif;">
        <!-- Phase 1 -->
        <div style="padding:1rem 1.5rem; border:2px solid #1f2937; border-radius:8px; max-width:500px; text-align:left; background:#f3f4f6;">
            <h3 style="margin:0 0 0.5rem 0;">Phase 1: Basic Console Navigation</h3>
            <ul>
                <li>Open developer tools confidently</li>
                <li>Navigate between Console and Elements tabs</li>
                <li>Execute simple JavaScript commands</li>
                <li>Read and interpret console output</li>
            </ul>
        </div>

        <!-- Arrow -->
        <div style="color:#1f2937; font-size:2.5rem;">&#8595;</div>

        <!-- Phase 2 -->
        <div style="padding:1rem 1.5rem; border:2px solid #1f2937; border-radius:8px; max-width:500px; text-align:left; background:#e5e7eb;">
            <h3 style="margin:0 0 0.5rem 0;">Phase 2: Function Interaction</h3>
            <ul>
                <li>Call functions with different parameters</li>
                <li>Understand how arguments affect results</li>
                <li>Recognize patterns in program behavior</li>
                <li>Predict outcomes based on code logic</li>
            </ul>
        </div>

        <!-- Arrow -->
        <div style="color:#1f2937; font-size:2.5rem;">&#8595;</div>

        <!-- Phase 3 -->
        <div style="padding:1rem 1.5rem; border:2px solid #1f2937; border-radius:8px; max-width:500px; text-align:left; background:#d1d5db;">
            <h3 style="margin:0 0 0.5rem 0;">Phase 3: Code Analysis</h3>
            <ul>
                <li>Read JavaScript code and understand its purpose</li>
                <li>Identify key programming concepts (variables, functions, conditionals)</li>
                <li>Trace execution flow from input to output</li>
                <li>Connect console results to underlying code logic</li>
            </ul>
        </div>
    </div>
</div>

<script>
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
</body>
</html>
</div>
