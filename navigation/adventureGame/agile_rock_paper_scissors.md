---
layout: base
title: Lesson Plan--> Can you play rock, paper, scissors shoot with us?
permalink: /gamify/rock_paper_scissors_shoot
---

## 🎮 Rock Paper Scissors Overview

This activity introduces students to **browser developer tools** — specifically the **Console** and **Inspect** features.  
By playing Rock Paper Scissors in the console, students learn how to:

- Interact with JavaScript functions  
- Track outputs  
- Explore how web applications respond behind the scenes  

---

## 🕹️ How to Play

1. Open this page in your browser.  
2. Right-click and choose **Inspect** (or press <kbd>Ctrl+Shift+I</kbd> on Windows / <kbd>Cmd+Option+I</kbd> on Mac).  
3. Go to the **Console** tab.  
4. Type one of these commands and press <kbd>Enter</kbd>:  
   - `playRPS("rock")`  
   - `playRPS("paper")`  
   - `playRPS("scissors")`  
5. Watch the console show your choice, the computer’s choice, and the result.  
6. Results also update in the game’s pop-up instructions box on the page.  

---

## ⚙️ Simplified Code Behind the Game

```javascript
window.playRPS = function(playerChoice) {
    const choices = ["rock", "paper", "scissors"];
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
};
```

---

## 🔍 Why Use Console Inspect?

The browser console is one of the most important debugging tools in web development. With it, you can:
- Test functions (`playRPS("rock")`)
- Print debugging info (`console.log`)
- See errors immediately
- Inspect elements in your HTML/CSS
- Experiment with live code changes  

---

## 💡 Why This Project Helps

By gamifying debugging, students:
- Get comfortable opening and using developer tools
- Understand how JavaScript functions can be tested without a GUI
- Learn to read console outputs to track logic
- See the cause–effect relationship between code and behavior
- Build confidence before tackling bigger debugging challenges  

---

## Reflection Questions

- **What information does the console give you that you can’t easily see on the webpage?**  
- **How could `console.log` statements help you fix bugs in bigger projects?**  
- **Why is testing functions directly in the console a useful skill for developers?**  
