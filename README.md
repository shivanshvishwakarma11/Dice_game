# Dice Game

A simple **Dice Game** built with **HTML, CSS, and JavaScript**. This game simulates rolling two dice, generating two random numbers, and compares them to determine the winner between **Player 1** and **Player 2**.

---

## Demo

![Dice Game Screenshot](screenshot.png)  
*Replace with your actual screenshot if available.*

---

## Features

- Two dice are rolled every time the page is reloaded or the **Roll Dice** button is clicked.
- Random numbers (1-6) are generated for both dice using JavaScript.
- The game compares the numbers to declare the winner:
  - Player 1 wins if their dice number is higher.
  - Player 2 wins if their dice number is higher.
  - It's a draw if both numbers are equal.
- Interactive and visually appealing with simple HTML and CSS styling.

---

## Technologies Used

- **HTML**: Structure of the dice game.
- **CSS**: Styling for dice and result display.
- **JavaScript**: Random number generation, comparison logic, and dynamic updates.

---

## How to Play

1. Open the `index.html` file in your browser.
2. Click on the **Roll Dice** button or reload the page.
3. The dice will roll and show random numbers for **Player 1** and **Player 2**.
4. The winner will be displayed based on the higher number.

---

## Code Snippet

**Random Number Generation and Comparison in JavaScript:**

```javascript
function rollDice() {
    const dice1 = Math.floor(Math.random() * 6) + 1;
    const dice2 = Math.floor(Math.random() * 6) + 1;

    document.getElementById('dice1').textContent = dice1;
    document.getElementById('dice2').textContent = dice2;

    let result = '';
    if(dice1 > dice2) {
        result = 'Player 1 Wins!';
    } else if(dice2 > dice1) {
        result = 'Player 2 Wins!';
    } else {
        result = "It's a Draw!";
    }

    document.getElementById('result').textContent = result;
}

window.onload = rollDice;
