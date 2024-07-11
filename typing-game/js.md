```js
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
  
let timeLeft = 5;
let score = 0;
let currentWord = "";
let timer;
let timeout;

const wordOrMessageBox = document.getElementById("word-or-message-box");
const wordInput = document.getElementById("word-input");
const timeDisplay = document.getElementById("time-left");
const scoreDisplay = document.getElementById("score");
const startButton = document.getElementById("start-button");
const resetButton = document.getElementById("reset-button");
const missedWordsBox = document.getElementById("missed-words-box");

startButton.addEventListener("click", startGame);
resetButton.addEventListener("click", resetGame);
wordInput.addEventListener("input", checkInput);

function startGame() {
  score = 0;
  wordInput.disabled = false;
  startButton.disabled = true;
  resetButton.disabled = false;
  scoreDisplay.textContent = score;
  timeDisplay.textContent = timeLeft;
  missedWordsBox.innerHTML = "";
  displayNewWord();
  timer = setInterval(updateTimeLeft, 1000);
}

function resetGame() {
  clearInterval(timer);
  clearTimeout(timeout);
  score = 0;
  timeLeft = 5;
  wordInput.disabled = true;
  startButton.disabled = false;
  resetButton.disabled = true;
  scoreDisplay.textContent = score;
  timeDisplay.textContent = timeLeft;
  wordOrMessageBox.textContent = "Click Start to Play!";
  wordInput.value = "";
  missedWordsBox.innerHTML = "";
}

function displayNewWord() {
  currentWord = words[Math.floor(Math.random() * words.length)];
  wordOrMessageBox.textContent = currentWord;
  timeLeft = 5;
  timeDisplay.textContent = timeLeft;
  wordInput.value = "";
  clearTimeout(timeout);
  timeout = setTimeout(handleNoTimeRemaining, timeLeft * 1000);
}

function updateTimeLeft() {
  timeLeft--;
  timeDisplay.textContent = timeLeft;
  if (timeLeft <= 0) {
    handleNoTimeRemaining();
  }
}

function handleNoTimeRemaining() {
  const missedWordBlock = document.createElement("div");
  missedWordBlock.classList.add("missed-word-block");
  missedWordBlock.textContent = currentWord;
  missedWordsBox.appendChild(missedWordBlock);
  checkGameOver();
  if (
    wordOrMessageBox.textContent !==
    "Game Over! Your score is " + score + ". Press Start to Play Again"
  ) {
    displayNewWord();
  }
}

function checkInput() {
  if (wordInput.value === currentWord) {
    score++;
    scoreDisplay.textContent = score;
    wordInput.value = "";
    displayNewWord();
  }
}

function checkGameOver() {
  const missedWordBlocks =
    missedWordsBox.querySelectorAll(".missed-word-block");

  if (missedWordBlocks.length >= 4) {
    clearInterval(timer);
    clearTimeout(timeout);
    wordInput.disabled = true;
    startButton.disabled = false;
    resetButton.disabled = true;
    wordOrMessageBox.textContent =
      "Game Over! Your score is " + score + ". Press Start to Play Again";
  }
}
```
