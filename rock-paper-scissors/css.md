```css
body {
  background: rgb(39, 212, 214);
  background: radial-gradient(
    circle,
    rgba(39, 212, 214, 1) 0%,
    rgba(216, 45, 253, 1) 100%
  );
}

.game {
  display: flex;
  justify-content: space-between;
  margin: 50px auto;
  max-width: 800px;
}

.player,
.computer {
  width: 45%;
  padding: 10px;
  border: 2px solid #333;
  border-radius: 5px;
}

.player {
  background-color: #f7f7f7;
}

.computer {
  background-color: #fff;
}

h2 {
  margin-top: 0;
}

.buttons {
  display: flex;
  justify-content: space-between;
}

button {
  font-size: 20px;
  padding: 10px 20px;
  border-radius: 5px;
  border: none;
  background-color: #333;
  color: #fff;
  cursor: pointer;
}

.result {
  margin-top: 10px;
  font-size: 24px;
  text-align: center;
}
```
