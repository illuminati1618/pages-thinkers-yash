---
layout: base
title: Rock Paper Scissors SHOOT!
permalink: /gamify/rock-paper-scissor
---
 
<div id="gameContainer">
    <canvas id='gameCanvas'></canvas>
</div>

<script type="module">
    // UI
    const instructionsStyle = `
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background: linear-gradient(135deg, black, purple);
        color: white;
        padding: 30px;
        border-radius: 15px;
        z-index: 1000;
        max-width: 600px;
        width: 90%;
        font-family: 'Press Start 2P', cursive;
        border: 3px solid purple;
        box-shadow: 0 0 20px rgba(128, 0, 128, 0.5);
        text-align: center;
    `;

    const instructionsHTML = `
        <h2 style="color: purple; margin-bottom: 20px;">Rock Paper Scissors SHOOT!</h2>
        <div style="margin-bottom: 20px;">
            <p>Play the game from your browser console!</p>
            <p>Type <code>playRPS("rock")</code>, <code>playRPS("paper")</code>, or <code>playRPS("scissors")</code></p>
        </div>
        <div id="images" style="display: flex; justify-content: center; gap: 20px; margin-bottom: 20px;">
            <button id="rock-btn" style="background:none; border:none; padding:0; cursor:pointer;">
                <img id="rock-img" src="{{site.baseurl}}/images/gamify/rock.jpg" 
                     style="width:100px; border:2px solid white; border-radius:10px;">
            </button>
            <button id="paper-btn" style="background:none; border:none; padding:0; cursor:pointer;">
                <img id="paper-img" src="{{site.baseurl}}/images/gamify/paper.jpeg" 
                     style="width:100px; border:2px solid white; border-radius:10px;">
            </button>
            <button id="scissors-btn" style="background:none; border:none; padding:0; cursor:pointer;">
                <img id="scissors-img" src="{{site.baseurl}}/images/gamify/scissors.jpeg" 
                     style="width:100px; border:2px solid white; border-radius:10px;">
            </button>
        </div>
        <div id="resultBox" style="margin-top: 25px; font-size: 16px; color: yellow;"></div>
    `;
    const container = document.createElement("div");
    container.setAttribute("style", instructionsStyle);
    container.innerHTML = instructionsHTML;
    document.body.appendChild(container);

    // Helper to highlight an image
    function highlightImage(id) {
        // Remove highlight from all
        ["rock-img", "paper-img", "scissors-img"].forEach(imgId => {
            const img = document.getElementById(imgId);
            if (img) img.style.boxShadow = "";
        });
        // Highlight selected
        const el = document.getElementById(id);
        if (el) el.style.boxShadow = "0 0 30px 10px gold";
    }

    // Rock-Paper-Scissors game logic
    window.playRPS = function(playerChoice) {
        const choices = ["rock", "paper", "scissors"];
        if (!choices.includes(playerChoice)) {
            console.log("Invalid choice. Use 'rock', 'paper', or 'scissors'.");
            return;
        }

        // Highlight the chosen element
        if (playerChoice === "rock") highlightImage("rock-img");
        if (playerChoice === "paper") highlightImage("paper-img");
        if (playerChoice === "scissors") highlightImage("scissors-img");

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

        console.log(`You chose: ${playerChoice.toUpperCase()}`);
        console.log(`Computer chose: ${computerChoice.toUpperCase()}`);
        console.log(`Result: ${resultText}`);

        document.getElementById("resultBox").innerHTML = `
            <p>You chose: <b>${playerChoice.toUpperCase()}</b></p>
            <p>Computer chose: <b>${computerChoice.toUpperCase()}</b></p>
            <h3 style="color: cyan;">${resultText}</h3>
        `;
    };

    // Add click events to images-as-buttons for inspect instructions
    document.getElementById("rock-btn").addEventListener("click", function() {
        alert(
            "🪨 Right-click this image and choose 'Inspect'!\n\nTry this in the console to change the border color:\n\ndocument.querySelector('#rock-img').style.border = '4px solid lime';"
        );
    });
    document.getElementById("paper-btn").addEventListener("click", function() {
        alert(
            "📄 Right-click this image and choose 'Inspect'!\n\nTry this in the console to rotate the image:\n\ndocument.querySelector('#paper-img').style.transform = 'rotate(15deg)';"
        );
    });
    document.getElementById("scissors-btn").addEventListener("click", function() {
        alert(
            "✂️ Right-click this image and choose 'Inspect'!\n\nTry this in the console to change the size:\n\ndocument.querySelector('#scissors-img').style.width = '150px';"
        );
    });
</script>