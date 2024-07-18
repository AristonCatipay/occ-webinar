```css
/* Root Styling */
:root {
  font-size: 1.5em;
}

/* General Styling */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

/* Game Area */
.game-area {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.word-div {
  font-size: 2em;
  margin-bottom: 20px;
  text-align: center;
  letter-spacing: 5px;
}

.attempts {
  display: flex;
  padding: 5px 10px;
  border: 1px solid #ccc;
  display: inline-block;
  margin-bottom: 20px;
  text-align: center;
}

/* Retry Button */
#retry-button {
  background-color: #4caf50;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  font-size: 1em;
  margin-bottom: 20px;
  cursor: pointer;
  border-radius: 5px;
}

#retry-button:hover {
  background-color: #45a049;
}

/* Custom Letter Buttons */
.keyboard {
  display: grid;
  grid-template-columns: repeat(10, 1fr);
  gap: 10px;
}

.letter {
  font-size: 1.5em;
  width: 70px;
  height: 70px;
  padding: 5px 10px;
  background-color: #068127;
  color: #fff;
  border: none;
  cursor: pointer;
  transition: all 0.125s ease;
  border-radius: 10px;
}

.letter:hover {
  filter: brightness(150%);
}

.letter:disabled {
  background-color: #616362;
}

/* Media Queries */
@media screen and (max-width: 1024px) {
  .keyboard {
    grid-template-columns: repeat(8, 1fr);
  }
}

@media screen and (max-width: 768px) {
  .keyboard {
    grid-template-columns: repeat(6, 1fr);
  }

  .letter {
    font-size: 1.2em;
  }

  .title {
    font-size: 1.6em;
  }
}

@media screen and (max-width: 481px) {
  .keyboard {
    grid-template-columns: repeat(4, 1fr);
  }

  .letter {
    font-size: 1em;
  }

  .title {
    font-size: 1.3em;
  }
}
```