```javascript
// Wait until the page is fully loaded
document.addEventListener("DOMContentLoaded", () => {
  // Get references to all the DOM elements we need
  const gameContainer = document.getElementById("game-container");
  const startButton = document.getElementById("start-button");
  const resetButton = document.getElementById("reset-button");
  const scoreDisplay = document.getElementById("score");
  const timerDisplay = document.getElementById("timer");

  // Initialize game variables
  let score = 0;
  let timeLeft = 20;
  let catTimer;
  let canClick = true;

  // Function to start the game
  function startGame() {
    startButton.style.display = "none";
    resetButton.style.display = "none";
    score = 0;
    timeLeft = 20;
    scoreDisplay.textContent = `SCORE: ${score}`;
    timerDisplay.textContent = `TIME: ${timeLeft} seconds`;
    spawnCat();
    catTimer = setInterval(spawnCat, 250); // Changed interval to 0.25 seconds (250)
    const gameTimer = setInterval(() => {
      timeLeft--;
      timerDisplay.textContent = `TIME: ${timeLeft} seconds`;
      if (timeLeft <= 0) {
        clearInterval(catTimer);
        clearInterval(gameTimer);
        endGame();
      }
    }, 1000);
  }

  // Function to spawn a new cat on the screen
  function spawnCat() {
    if (!canClick) return;
    const cat = document.getElementById("cat");
    if (cat) gameContainer.removeChild(cat);
    const newCat = document.createElement("img");
    newCat.src =
      "https://i.pinimg.com/originals/5f/93/49/5f934966a1d20bae1909c9ef2278bd4c.gif";
    newCat.id = "cat";
    newCat.style.left = `${Math.random() * 200}px`;
    newCat.style.top = `${Math.random() * 200}px`;
    newCat.addEventListener("click", () => {
      if (!canClick) return;
      score++;
      scoreDisplay.textContent = `SCORE: ${score}`;
      gameContainer.removeChild(newCat);
    });
    gameContainer.appendChild(newCat);
  }

  // Function to handle the end of the game
  function endGame() {
    startButton.style.display = "none";
    resetButton.style.display = "block";
    scoreDisplay.textContent = `GAME OVER! \nFinal Score: ${score}`;
    timerDisplay.textContent = "";
    canClick = false;
  }

  //Add event listeners
  startButton.addEventListener("click", startGame);
  resetButton.addEventListener("click", () => {
    startButton.style.display = "none";
    resetButton.style.display = "none";
    canClick = true;
    startGame();
  });
});
```
