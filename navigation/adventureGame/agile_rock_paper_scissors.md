---
layout: base
title: Lesson Plan--> Can you play rock, paper, scissors shoot with us?
permalink: /gamify/rock_paper_scissors_shoot
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

1. **Access Developer Tools**
   - Right-click anywhere on this page
   - Select "Inspect" or "Inspect Element" from the menu
   - Alternative: Use keyboard shortcuts
     - Windows/Linux: `Ctrl + Shift + I`
     - Mac: `Cmd + Option + I`

2. **Navigate to Console**
   - Look for tabs at the top of the developer panel
   - Click "Console" to switch to the interactive environment
   - You should see a command prompt (usually `>` symbol)

3. **Execute Game Commands**
   - Type exactly: `playRPS("rock")` and press Enter
   - Try other choices: `playRPS("paper")` or `playRPS("scissors")`
   - Watch the console display your results in real-time

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

### Progressive Skill Development

**Phase 1: Basic Console Navigation**
1. Open developer tools confidently
2. Navigate between Console and Elements tabs  
3. Execute simple JavaScript commands
4. Read and interpret console output

**Phase 2: Function Interaction**  
1. Call functions with different parameters
2. Understand how arguments affect results
3. Recognize patterns in program behavior
4. Predict outcomes based on code logic

**Phase 3: Code Analysis**
1. Read JavaScript code and understand its purpose
2. Identify key programming concepts (variables, functions, conditionals)
3. Trace execution flow from input to output
4. Connect console results to underlying code logic

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