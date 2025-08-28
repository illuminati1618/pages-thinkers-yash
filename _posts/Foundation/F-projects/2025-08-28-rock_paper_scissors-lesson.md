---
layout: opencs
title: Lesson Plan Can you play rock, paper, scissors shoot with us
permalink: /rock_paper_scissors/lessons
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rock Paper Scissors Console Learning</title>
    <style>
      /* Force light mode and prevent browser overrides */
          :root {
              color-scheme: dark !important;
          }
          body, body * {
              color: #e5e7eb !important;
              background: #18181b !important;
          }
          /* Ensure high contrast */
          h1, h2, h3, h4, h5, h6 {
              color: #ffffffff !important;
          }
          p, li, span, div {
              color: #ffffffff !important;
          }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #ffffffff;
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
            border: 3px solid #090801ff;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        h1 {
            color: #ffffffff;
            text-align: center;
            font-size: 2.5em;
            margin-bottom: 10px;
            border-bottom: 3px solid #020000ff;
            padding-bottom: 10px;
            font-weight: bold;
        }
        h2 {
            color: #ffffffff;
            font-size: 1.8em;
            border-left: 4px solid #c06c84;
            padding-left: 15px;
            margin-top: 30px;
            font-weight: bold;
        }
        h3 {
            color: #ffffffff;
            font-size: 1.4em;
            margin-top: 25px;
            font-weight: bold;
        }
        h4 {
            color: #ffffffff;
            font-size: 1.2em;
            margin-top: 20px;
            font-weight: bold;
        }
        .subtitle {
            text-align: center;
            color: #ffffffff;
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
        /* OOP and Console Commands code blocks: black bg, white text */
        .code-block {
            background: #1a1a1a;
            color: #fff !important;
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

    <div style="text-align:center; margin-bottom:24px; color:#ffffffff; font-size:1.1em;">
        Click any icon to customize using the console
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
            <h4>What is the Console and Why is it Powerful?</h4>
            <p>
                The browser console is a built-in tool for developers to interact with web pages using JavaScript. It allows you to run code, inspect variables, debug errors, and even change how a page looks or behaves in real time. The console is like a playground for experimentation and learning.
            </p>
            <ul>
                <li><strong>Debugging:</strong> You can see error messages, warnings, and logs that help you find and fix problems in your code.</li>
                <li><strong>Live Coding:</strong> Type any JavaScript command and see the result instantly. This is great for testing ideas or learning how code works.</li>
                <li><strong>Inspecting Objects:</strong> You can explore the properties and methods of any object, including elements on the page, by typing their names in the console.</li>
                <li><strong>Changing the Page:</strong> You can modify HTML, CSS, and even run scripts to change how the page looks or behaves, all without reloading.</li>
                <li><strong>Learning Tool:</strong> The console is perfect for beginners to experiment with code, see immediate feedback, and build confidence in programming.</li>
                <li><strong>Advanced Features:</strong> You can profile performance, monitor network requests, and automate repetitive tasks using the console.</li>
            </ul>
            <p>
                <strong>Example:</strong> Try typing <code>document.body.style.background = '#222'</code> in the console to instantly change the page background color. Or use <code>console.log('Hello!')</code> to print a message. The console is your direct line to the browser's engine.
            </p>
            <p>
                <strong>Why use the console in this lesson?</strong> By playing Rock Paper Scissors in the console, you learn how to call functions, pass arguments, and see results. You also get comfortable with the developer tools, which are essential for any web developer.
            </p>
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
                  <li>Type exactly: playRPS(&quot;rock&quot;) and press Enter</li>
                  <li>Try other choices: playRPS(&quot;paper&quot;) or playRPS(&quot;scissors&quot;)</li>
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
        <div style="padding:1rem 1.5rem; border:2px solid #ffffffff; border-radius:8px; max-width:500px; text-align:left; background:#f3f4f6;">
            <h3 style="margin:0 0 0.5rem 0;">Phase 1: Basic Console Navigation</h3>
            <ul>
                <li>Open developer tools confidently</li>
                <li>Navigate between Console and Elements tabs</li>
                <li>Execute simple JavaScript commands</li>
                <li>Read and interpret console output</li>
            </ul>
        </div>

        <!-- Arrow -->
        <div style="color:#ffffffff; font-size:2.5rem;">&#8595;</div>

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

    <h2>Object-Oriented Programming (OOP) in Rock Paper Scissors</h2>
    <p>
        <strong>What is OOP?</strong><br>
        Object-Oriented Programming (OOP) is a programming paradigm that focuses on organizing code into <strong>objects</strong>. Each object combines both <em>data</em> and <em>functions</em> (called methods) that operate on that data. Rather than writing long scripts where variables and functions are scattered throughout the code, OOP allows developers to group related functionality and information into self-contained units. This makes the code easier to manage, understand, and extend over time.
    </p>

    <p>
        Objects can represent real-world entities, such as cars, buttons, or even players in a game. Each object has <strong>properties</strong> (attributes that describe it) and <strong>methods</strong> (actions it can perform). For example, in a car simulation, a <code>Car</code> object might have properties like <code>color</code>, <code>speed</code>, and <code>fuelLevel</code>, and methods like <code>accelerate()</code>, <code>brake()</code>, and <code>refuel()</code>.  
    </p>

    <p>
        One of the key advantages of OOP is <strong>encapsulation</strong>. This means that the internal workings of an object are hidden from the outside world, and interaction occurs through well-defined methods. For example, when you call <code>car.accelerate()</code>, you don't need to know exactly how the car updates its speed internally—you just know the outcome. This makes code more modular, reduces errors, and allows developers to focus on higher-level logic.
    </p>

    <p>
        Another advantage is <strong>reusability</strong>. Once an object or class is created, it can be reused across different parts of a program or even in different programs. For instance, a <code>Button</code> class for a game can be reused in multiple games with minimal changes. OOP also promotes <strong>extensibility</strong>, meaning you can create new objects based on existing ones and add or modify functionality without rewriting the original code. This is typically done through <strong>inheritance</strong>.
    </p>

    <hr>

    <p>
        <strong>How to add OOP in code?</strong><br>
        In JavaScript, OOP is implemented primarily through the use of <strong>classes</strong> and <strong>objects</strong>. A <code>class</code> serves as a blueprint for creating objects, specifying which properties and methods each object will have. Classes help you organize your code and avoid repetitive coding patterns.
    </p>

    <p>
        For example, consider a game where players interact with buttons. You could create a <code>Button</code> class to define all buttons' common properties and behaviors. This class could include properties like <code>positionX</code>, <code>positionY</code>, <code>color</code>, and <code>size</code>. It could also include methods like <code>move()</code>, <code>animate()</code>, <code>highlight()</code>, or <code>reset()</code> to define what each button does in response to user actions.
    </p>

    <p>
        You might also create a <code>Game</code> class to manage the overall logic of your game. This class could include properties like <code>score</code>, <code>round</code>, <code>playerChoices</code>, and methods like <code>startRound()</code>, <code>determineWinner()</code>, and <code>endGame()</code>. By creating instances of these classes (objects), you can handle multiple buttons and multiple game instances without duplicating code.
    </p>

    <p>
        JavaScript also allows <strong>inheritance</strong>, where a new class can extend an existing one and inherit its properties and methods. For example, you could create a <code>SpecialButton</code> class that inherits from <code>Button</code> but has additional properties like <code>animationType</code> or <code>specialEffect()</code>. This allows you to build complex systems incrementally, without starting from scratch each time.
    </p>

    <p>
        Another important OOP concept is <strong>polymorphism</strong>, which allows objects of different classes to respond to the same method in different ways. For example, both a <code>NormalButton</code> and a <code>SpecialButton</code> might have an <code>animate()</code> method, but the animation behavior can differ based on the button type.
    </p>

    <hr>

    <p>
        <strong>How do we use OOP here?</strong><br>
        In this game, OOP is used to manage buttons, animations, and interactions in a structured way. Each button is represented as an object with its own properties, such as position, size, color, and state (active, inactive, or disabled). Each button object also contains methods that define its behavior, such as moving, animating, or responding to a click event.
    </p>

    <p>
        When a player makes a move, the game logic (handled by the <code>Game</code> object) determines the winner and the loser. The winning button then animates dynamically—moving over the losing button, bouncing, changing color, or displaying special effects. Because each button is an object, it controls its own animation and behavior independently of other buttons. This modularity makes the code flexible, easy to maintain, and easy to expand.
    </p>

    <p>
        Adding new button types or changing animations is simple. You can create a new class that extends the original <code>Button</code> class and override or add methods for new behavior, leaving existing button objects untouched. This also makes debugging much easier, since problems can usually be isolated to a specific object or method.
    </p>

    <p>
        By using OOP, the game becomes a system of interacting objects. Each object has clearly defined responsibilities, which helps organize the logic of complex interactions like determining winners, animating movements, and updating scores. The separation of responsibilities between objects, such as <code>Button</code> and <code>Game</code>, ensures that each part of the program is easier to understand, modify, and expand.
    </p>

    <hr>

    <p>
        <strong>Why OOP is especially useful in games</strong><br>
        Games often involve multiple interactive elements that change state, respond to user input, and animate in real time. OOP allows each element to be represented as an object with its own properties and methods, which simplifies the management of complex behaviors.
    </p>

    <p>
        For example, in a rock-paper-scissors game, each choice can be an object that knows how to respond when selected, how to animate when it wins, and how to reset when the round ends. Without OOP, coordinating all these behaviors would require repetitive procedural code and complex conditionals, which would be harder to debug and maintain.
    </p>

    <p>
        Using OOP also makes it easier to implement advanced features such as dynamic animations, visual effects, and interactive feedback. Each object can manage its own state and behavior while communicating with other objects when necessary. This allows developers to focus on defining individual behaviors and letting interactions emerge naturally from the combination of objects.
    </p>

    <p>
        Overall, OOP improves <strong>readability</strong>, <strong>maintainability</strong>, and <strong>scalability</strong> in game development. It encourages thinking in terms of real-world entities, allows for modular code, and provides a robust framework for creating complex, interactive, and visually dynamic games.
    </p>

    <hr>

    <p>
        <strong>Additional tips for using OOP in games:</strong><br>
        1. Start by identifying the main objects in your game, such as buttons, players, enemies, or game boards.<br>
        2. Define properties for each object that describe its state.<br>
        3. Define methods for each object that describe its behavior.<br>
        4. Use inheritance to create specialized versions of objects without duplicating code.<br>
        5. Keep each object responsible for its own behavior to maintain modularity.<br>
        6. Test objects individually before integrating them into the main game logic.<br>
        7. Use polymorphism when multiple object types share common behavior but differ in implementation.
    </p>

    <hr>

    <p>
        <strong>Summary:</strong>
    </p>
    <ul>
        <li>OOP organizes code into objects that combine data and behavior.</li>
        <li>Objects have properties (state) and methods (actions).</li>
        <li>Classes are blueprints for creating objects.</li>
        <li>Encapsulation hides internal details and promotes modularity.</li>
        <li>Inheritance allows new objects to reuse and extend existing ones.</li>
        <li>Polymorphism enables objects to respond differently to the same methods.</li>
        <li>OOP makes game development more manageable, scalable, and maintainable.</li>
        <li>Each game element (like buttons) can be an object managing its own behavior and animation.</li>
        <li>Using OOP, interactions emerge naturally from the combined behaviors of objects.</li>
        <li>It simplifies debugging, adding new features, and creating dynamic animations.</li>
    </ul>


    <div class="console-example" style="background:#cce7ff; color:#0f0;">
        <pre>
class GameButton {
    constructor(element) {
        this.element = element;
    }
    animateOver(target) {
        // Move this button over the target button
    }
}
        </pre>
    </div>

    <h2>Console Commands</h2>
    <p>
        Each button is customizable using the browser console. Try these commands to change their appearance:
    </p>
    <ul>
        <li>
            <strong>Rock:</strong> Change border color<br>
            <div class="code-block">document.querySelector('button[onclick="playRPS(\'rock\')"]').style.border = '4px solid lime';</div>
        </li>
        <li>
            <strong>Paper:</strong> Rotate the button<br>
            <div class="code-block">document.querySelector('button[onclick="playRPS(\'paper\')"]').style.transform = 'rotate(15deg)';</div>
        </li>
        <li>
            <strong>Scissors:</strong> Change button size<br>
            <div class="code-block">document.querySelector('button[onclick="playRPS(\'scissors\')"]').style.fontSize = '2em';</div>
        </li>
            <li>
                <strong>All Buttons:</strong> Add a glowing effect<br>
                <div class="code-block">document.querySelectorAll('button').forEach(btn => btn.style.boxShadow = '0 0 20px #ffd700');</div>
            </li>
            <li>
                <strong>Reset Styles:</strong> Remove all custom styles<br>
                <div class="code-block">document.querySelectorAll('button').forEach(btn => { btn.style.border = ''; btn.style.transform = ''; btn.style.fontSize = ''; btn.style.boxShadow = ''; });</div>
            </li>
            <li>
                <strong>Change Text:</strong> Update button labels<br>
                <div class="code-block">document.querySelector('button[onclick="playRPS(\'rock\')"]').textContent = 'Boulder';</div>
            </li>
            <li>
                <strong>Disable Button:</strong> Prevent clicking a button<br>
                <div class="code-block">document.querySelector('button[onclick="playRPS(\'scissors\')"]').disabled = true;</div>
            </li>
            <li>
                <strong>Log All Buttons:</strong> Print all button elements to the console<br>
                <div class="code-block">console.log(document.querySelectorAll('button'));</div>
            </li>
            <li>
                <strong>Change Background:</strong> Set the container background to blue<br>
                <div class="code-block">document.querySelector('.container').style.background = '#1e3a8a';</div>
            </li>
            <li>
                <strong>Make Buttons Circular:</strong> Change button shape<br>
                <div class="code-block">document.querySelectorAll('button').forEach(btn => btn.style.borderRadius = '50%');</div>
            </li>
            <li>
                <strong>Animate Button:</strong> Make a button pulse<br>
                <div class="code-block">let btn = document.querySelector('button[onclick="playRPS(\'rock\')"]'); btn.style.transition = 'transform 0.3s'; btn.style.transform = 'scale(1.2)'; setTimeout(() => btn.style.transform = 'scale(1)', 300);</div>
            </li>
            <li>
                <strong>Change Font:</strong> Set all button text to a new font<br>
                <div class="code-block">document.querySelectorAll('button').forEach(btn => btn.style.fontFamily = 'Comic Sans MS');</div>
            </li>
            <li>
                <strong>Hide Buttons:</strong> Remove all buttons from view<br>
                <div class="code-block">document.querySelectorAll('button').forEach(btn => btn.style.display = 'none');</div>
            </li>
            <li>
                <strong>Show Buttons:</strong> Restore all buttons<br>
                <div class="code-block">document.querySelectorAll('button').forEach(btn => btn.style.display = '');</div>
            </li>
    </ul>
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

