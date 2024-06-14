```css
* {
  font-family: Arial, sans-serif;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  color: #2f184b;
}

html,
body {
  height: 100vh;
}

body {
  text-align: center;
  background-color: #f4f1de;
  display: flex;
  justify-content: center;
  align-items: center;
}

#word-box {
  font-size: 24px;
  margin-bottom: 10px;
}

#game-box {
  background-color: #f4f1de;
  width: 300px;
  height: 220px;
  margin: 0 auto;
  border: 10px solid #3d405b;
  border-radius: 5px;
  box-shadow: 5px 5px 8px rgba(0, 0, 0, 0.3);
  overflow: hidden;
}

.block {
  background-color: #3d405b;
  height: 50px;
  padding: 10px;
  color: white;
  border: 5px solid #f4f1de;
}

#word-input {
  background-color: #f4f1de;
  width: 300px;
  margin: 20px;
  padding: 10px;
  font-size: 18px;
  text-align: center;
  border: 5px solid #3d405b;
  border-radius: 5px;
  box-shadow: 5px 5px 8px rgba(0, 0, 0, 0.3);
}

#word-input:focus {
  box-shadow: 5px 5px 8px rgba(233, 79, 55, 0.692);
  outline: none;
}

.button-container {
  margin: 20px;
  display: flex;
  justify-content: center;
  gap: 10px;
}

button {
  background-color: #e94f37;
  padding: 10px 20px;
  font-size: 16px;
  color: #f4effa;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  box-shadow: 5px 5px 8px rgba(0, 0, 0, 0.3);
}

button:hover {
  transform: scale(1.2);
}

button:disabled{
  background-color: #e07a5f;
  pointer-events: none;
  cursor: not-allowed;
}

#time-left,
#score {
  font-weight: bold;
  color: #3d405b;
}
```