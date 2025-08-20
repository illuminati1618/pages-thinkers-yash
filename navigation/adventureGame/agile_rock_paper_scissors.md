---
layout: base
title: Lesson Plan--> Can you play rock, paper, scissors shoot with us?
permalink: /gamify/rock_paper_scissors_shoot
css: "/assets/css/rockpaper.css"
---
## Rock Paper Scissors Console Learning

*A hands-on introduction to browser developer tools through interactive gameplay*

---

## What is Browser Console Development?

Browser developer tools are built-in debugging environments that let you interact with web pages behind the scenes. The **Console** is where developers test JavaScript code, debug programs, and explore how web applications work in real-time.

### Understanding the Developer Tools Interface

**Console Tab Features:**
- **Interactive JavaScript Environment:** Type commands and see immediate results
- **Function Testing:** Call functions directly without needing buttons or forms  
- **Output Tracking:** View `console.log()` statements and error messages
- **Live Code Execution:** Test code changes without modifying source files

**Inspect Element Features:**
- **HTML Structure:** See the actual markup that creates the webpage
- **CSS Styling:** View and modify styles applied to elements
- **Network Activity:** Monitor requests and responses between browser and server

---

## The Rock Paper Scissors Console Game

This interactive lesson teaches console navigation through a familiar game. Instead of clicking buttons, you'll execute JavaScript functions directly in the console.

### Game Setup Process

**Step-by-Step Instructions:**

<div style="display:flex; align-items:flex-start; max-width:1100px; margin:0 auto;">
  <figure style="float:left; width:400px; margin:0 4rem 4rem 0; text-align:center;">
    <img
      src="{{site.baseurl}}/images/gamify/flowchart_console.png"
      alt="Infographic: How to use the browser console — Open Dev Tools, Navigate to Console, Type Command, See Results"
      style="width:100%; height:auto; display:block; border-radius:8px; box-shadow:0 6px 18px rgba(0,0,0,0.08);"
    />
  </figure>
  <div style="flex:1; min-width:350px; max-width:700px;">
  <ul style="margin:0; padding-left:0.2rem; list-style-type: disc; list-style-position: outside;">
      <li><strong>Access Developer Tools</strong>
        <ul style="margin:0; padding-left:2rem; list-style-type: circle; list-style-position: outside;">
          <li>Right-click anywhere on this page</li>
          <li>Select "Inspect" or "Inspect Element" from the menu</li>
          <li>Alternative: Use keyboard shortcuts
            <ul style="margin:0; padding-left:3rem; list-style-type: square; list-style-position: outside;">
              <li>Windows/Linux: <code>Ctrl + Shift + I</code></li>
              <li>Mac: <code>Cmd + Option + I</code></li>
            </ul>
          </li>
        </ul>
      </li>
      <li><strong>Navigate to Console</strong>
        <ul style="margin:0; padding-left:2rem; list-style-type: circle; list-style-position: outside;">
          <li>Look for tabs at the top of the developer panel</li>
          <li>Click "Console" to switch to the interactive environment</li>
          <li>You should see a command prompt (usually <code>&gt;</code> symbol)</li>
        </ul>
      </li>
      <li><strong>Run Commands</strong>
        <ul style="margin:0; padding-left:2rem; list-style-type: circle; list-style-position: outside;">
          <li>Type exactly: <code>playRPS("rock")</code> and press Enter</li>
          <li>Try other choices: <code>playRPS("paper")</code> or <code>playRPS("scissors")</code></li>
          <li>Watch the console display your results in real-time</li>
        </ul>
      </li>
    </ul>
  </div>
</div>

<div style="clear:both;"></div>
### Sample Console Interaction


```
> playRPS("rock")
You chose: ROCK
Computer chose: SCISSORS  
Result: You Win!

> playRPS("paper")
You chose: PAPER
Computer chose: PAPER
Result: Tie!
```

---

## How the Game Logic Works

Understanding the code helps you see how console interaction connects to JavaScript execution:

```javascript
window.playRPS = function(playerChoice) {
    // Array of possible choices
    const choices = ["rock", "paper", "scissors"];
    
    // Computer makes random selection
    const computerChoice = choices[Math.floor(Math.random() * choices.length)];

    // Game logic determines winner
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

    // Output results to console
    console.log(`You chose: ${playerChoice.toUpperCase()}`);
    console.log(`Computer chose: ${computerChoice.toUpperCase()}`);
    console.log(`Result: ${resultText}`);
};
```

### Key Programming Concepts Demonstrated

**Function Definition:** `window.playRPS = function(playerChoice)` creates a globally accessible function

**Random Selection:** `Math.floor(Math.random() * choices.length)` generates unpredictable computer choices

**Conditional Logic:** Multiple `if/else` statements determine win/lose/tie outcomes

**Console Output:** `console.log()` statements provide immediate feedback to developers

---

## Why Console Development Matters

### Essential Developer Skills

**Debugging Capabilities:**
- **Immediate Feedback:** Test functions without building full user interfaces
- **Error Detection:** Spot syntax errors and logic problems quickly  
- **Variable Inspection:** Check what values your code is actually producing
- **Performance Monitoring:** See how fast your functions execute

**Professional Development Workflow:**
- **Rapid Prototyping:** Try out ideas before writing full applications
- **API Testing:** Test external services and data connections
- **DOM Manipulation:** Modify webpage elements in real-time
- **Script Injection:** Add functionality to existing websites

### Real-World Applications

**Web Development:**
- Debug JavaScript before deployment
- Test user interface interactions
- Verify API responses and data handling
- Optimize page loading performance

**Learning Programming:**
- Understand cause-and-effect relationships in code
- Practice JavaScript syntax without complex setup
- Explore how existing websites implement features
- Build confidence with interactive programming

---

## Learning Workflow

<div style="display:flex; flex-direction:column; align-items:center; gap:1rem; margin:2rem 0; font-family:sans-serif; background:#222; padding:2rem;">

  <!-- Phase 1 -->
  <div style="padding:1rem 1.5rem; border:2px solid #fff; border-radius:8px; max-width:500px; text-align:left; color:#fff;">
    <h3 style="margin:0 0 0.5rem 0;">Phase 1: Basic Console Navigation</h3>
    <ul style="margin:0; padding-left:1.2rem;">
      <li>Open developer tools confidently</li>
      <li>Navigate between Console and Elements tabs</li>
      <li>Execute simple JavaScript commands</li>
      <li>Read and interpret console output</li>
    </ul>
  </div>

  <!-- Arrow -->
  <div style="color:#fff; font-size:3rem; line-height:3rem;">&#8595;</div>

  <!-- Phase 2 -->
  <div style="padding:1rem 1.5rem; border:2px solid #fff; border-radius:8px; max-width:500px; text-align:left; color:#fff;">
    <h3 style="margin:0 0 0.5rem 0;">Phase 2: Function Interaction</h3>
    <ul style="margin:0; padding-left:1.2rem;">
      <li>Call functions with different parameters</li>
      <li>Understand how arguments affect results</li>
      <li>Recognize patterns in program behavior</li>
      <li>Predict outcomes based on code logic</li>
    </ul>
  </div>

  <!-- Arrow -->
  <div style="color:#fff; font-size:3rem; line-height:3rem;">&#8595;</div>

  <!-- Phase 3 -->
  <div style="padding:1rem 1.5rem; border:2px solid #fff; border-radius:8px; max-width:500px; text-align:left; color:#fff;">
    <h3 style="margin:0 0 0.5rem 0;">Phase 3: Code Analysis</h3>
    <ul style="margin:0; padding-left:1.2rem;">
      <li>Read JavaScript code and understand its purpose</li>
      <li>Identify key programming concepts (variables, functions, conditionals)</li>
      <li>Trace execution flow from input to output</li>
      <li>Connect console results to underlying code logic</li>
    </ul>
  </div>

</div>
---


## Key Learning Outcomes

### Technical Skills Gained

**Console Proficiency:**
- Navigate browser developer tools efficiently
- Execute JavaScript commands with confidence
- Interpret console output and error messages
- Use console for debugging and experimentation

**Code Comprehension:**
- Read JavaScript functions and understand their logic
- Recognize common programming patterns (conditionals, random selection)
- Connect function parameters to program behavior
- Understand the relationship between code and console output

**Problem-Solving Mindset:**
- Use console testing to verify code behavior
- Approach debugging systematically through direct testing
- Build comfort with trial-and-error learning in programming
- Develop intuition for how web applications work internally

---

## Reflection & Extension Activities

### Critical Thinking Questions

**Technical Understanding:**
- What advantages does console testing have over clicking buttons on a webpage?
- How do `console.log()` statements help developers understand what their code is doing?
- Why might professional developers prefer command-line interfaces for testing?

**Code Analysis:**
- Can you identify where the random computer choice gets generated in the code?
- What would happen if you called `playRPS("banana")` instead of a valid choice?
- How could you modify the game to include additional choices like "lizard" and "spock"?

**Skill Transfer:**
- How could console debugging help you in other programming projects?
- What other types of functions might be useful to test directly in the console?
- When might you choose console interaction over graphical user interfaces?

### Extension Challenges

**Beginner:**
- Try calling the function with invalid inputs and observe error handling
- Use the console to call the function multiple times quickly
- Explore other console methods like `console.warn()` or `console.error()`

**Intermediate:**
- Modify the game logic to track wins/losses across multiple games
- Create your own simple function and test it in the console
- Investigate what other JavaScript functions are available on this webpage

**Advanced:**
- Research how to save console commands as bookmarks for reuse
- Learn about console debugging techniques used in professional development
- Explore how console interaction differs across various web browsers

---

## Success Indicators
- Can open developer tools and navigate to console
- Successfully executes `playRPS()` function with valid parameters
- Understands relationship between function calls and console output
- Explains how the game logic determines winners
- Recognizes the role of `Math.random()` in computer choice selection  
- Connects `console.log()` statements to visible output
- Uses console confidently for testing and experimentation
- Applies console debugging skills to other programming contexts
- Demonstrates understanding of when console interaction is preferable to GUI testing

This foundation prepares students for more advanced web development concepts while building confidence through playful, hands-on interaction with professional developer tools.