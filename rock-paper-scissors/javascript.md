```javascript
// Define an array of possible moves
const moves = ["rock", "paper", "scissors"];

// Get the game elements from the HTML page
const rockBtn = document.querySelector("#rock");
const paperBtn = document.querySelector("#paper");
const scissorsBtn = document.querySelector("#scissors");
const gameResult = document.querySelector(".result");

// Add event listeners to the buttons
rockBtn.addEventListener("click", function () {
  playGame("rock");
});
paperBtn.addEventListener("click", function () {
  playGame("paper");
});
scissorsBtn.addEventListener("click", function () {
  playGame("scissors");
});

// Define the function to play the game
function playGame(playerMove) {
  // Generate a random move for the computer
  const computerMove = moves[Math.floor(Math.random() * moves.length)];

  // Determine the winner using if-else statements
  if (playerMove === computerMove) {
    gameResult.textContent = computerMove + "!" + " " + "It's a tie!";
  } else if (
    (playerMove === "rock" && computerMove === "scissors") ||
    (playerMove === "paper" && computerMove === "rock") ||
    (playerMove === "scissors" && computerMove === "paper")
  ) {
    gameResult.textContent = computerMove + "!" + " " + "You win!";
  } else {
    gameResult.textContent = computerMove + "!" + " " + "Computer wins!";
  }
}
```
