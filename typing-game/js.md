```js
document.addEventListener("DOMContentLoaded", () => {
  const words = [
    "abstract", "beautiful", "chocolate", "dynamite", "elephant", "fantastic",
    "gorgeous", "happiness", "invisible", "jubilant", "knowledge", "luminous",
    "magnificent", "nightmare", "opulent", "picturesque", "quizzical", "resilient",
    "symphony", "twilight", "umbrella", "vibrant", "whimsical", "xylophone",
    "yesterday", "zealous", "adventure", "butterfly", "crystalline", "diligent",
    "enchanted", "fascinate", "glorious", "harmonious", "illusion", "jovial",
    "kaleidoscope", "labyrinth", "melancholy", "nostalgia", "optimistic", "paradise",
    "quintessential", "radiant", "serendipity", "tranquility", "universe", "victorious",
    "whirlwind", "xenophobia", "youthful", "zephyr", "ambitious", "brilliant", 
    "celebrate", "delightful", "effervescent", "flourish", "gratitude", "horizon", 
    "inspiration", "jubilation", "kudos", "luminary", "momentous", "nurture", 
    "overjoyed", "phenomenal", "quicksilver", "remarkable", "spectacular", "tremendous"
  ];  
  
  let wordTimeLeft = 5;
  let overallScore = 0;
  let currentWord = "";
  let countdownTimer;
  let wordTimeout;

  const wordBox = document.getElementById("word-box");
  const wordInput = document.getElementById("word-input");
  const wordTimeLeftDisplay = document.getElementById("time-left");
  const overallScoreDisplay = document.getElementById("score");
  const startButton = document.getElementById("start-button");
  const resetButton = document.getElementById("reset-button");
  const gameBox = document.getElementById("game-box");

  function startGame() {
    wordTimeLeft = 5;
    overallScore = 0;
    wordInput.value = "";
    wordInput.disabled = false;
    wordInput.focus();
    startButton.disabled = true;
    resetButton.disabled = false;
    overallScoreDisplay.textContent = overallScore;
    wordTimeLeftDisplay.textContent = wordTimeLeft;
    clearGameBox();
    displayNewWord();
    countdownTimer = setInterval(updateWordTimeLeft, 1000);
  }

  function resetGame() {
    clearInterval(countdownTimer);
    clearTimeout(wordTimeout);
    wordInput.disabled = true;
    startButton.disabled = false;
    resetButton.disabled = true;
    overallScore = 0;
    overallScoreDisplay.textContent = overallScore;
    wordTimeLeft = 5;
    wordTimeLeftDisplay.textContent = wordTimeLeft;
    wordBox.textContent = "Click the start button to start the game!";
    wordInput.value = "";
    clearGameBox();
  }

  function clearGameBox() {
    while (gameBox.firstChild) {
      gameBox.removeChild(gameBox.firstChild);
    }
  }

  function displayNewWord() {
    const randomIndex = Math.floor(Math.random() * words.length);
    currentWord = words[randomIndex];
    wordBox.textContent = currentWord;
    wordTimeLeft = 5;
    wordTimeLeftDisplay.textContent = wordTimeLeft;
    wordInput.value = "";
    clearTimeout(wordTimeout);
    wordTimeout = setTimeout(handleWordTimeout, wordTimeLeft * 1000);
  }

  function updateWordTimeLeft() {
    wordTimeLeft--;
    wordTimeLeftDisplay.textContent = wordTimeLeft;
    if (wordTimeLeft <= 0) {
      handleWordTimeout();
    }
  }

  function handleWordTimeout() {
    if (wordBox.textContent === currentWord) {
      const block = document.createElement("div");
      block.className = "block";
      block.textContent = currentWord;
      gameBox.appendChild(block);
      checkGameOver();
      if (
        wordBox.textContent !==
        `Game Over! Your score is ${overallScore}. Press Start to Play Again`
      ) {
        displayNewWord();
      }
    }
  }

  function checkInput() {
    if (wordInput.value === currentWord) {
      overallScore++;
      overallScoreDisplay.textContent = overallScore;
      wordInput.value = "";
      displayNewWord();
    }
  }

  function checkGameOver() {
    const blocks = document.querySelectorAll("#game-box .block");

    if (blocks.length >= 4) {
      clearInterval(countdownTimer);
      clearTimeout(wordTimeout);
      wordInput.disabled = true;
      startButton.disabled = false;
      resetButton.disabled = true;
      wordBox.textContent = `Game Over! Your score is ${overallScore}. Press Start to Play Again`;
    }
  }

  startButton.addEventListener("click", startGame);
  resetButton.addEventListener("click", resetGame);
  wordInput.addEventListener("input", checkInput);
});
```