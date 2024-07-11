```html
<div class="game-container">
  <h1>Typing Game</h1>
  <div id="word-or-message-box">Click the start button to start the game!</div>
  <div id="missed-words-box"></div>
  <input
    type="text"
    id="word-input"
    placeholder="Type the word here..."
    disabled
  />
  <p>Time Left: <span id="time-left">5</span> seconds</p>
  <p>Score: <span id="score">0</span></p>
  <div class="button-container">
    <button id="start-button">Start Game</button>
    <button id="reset-button" disabled>Reset</button>
  </div>
</div>
```
