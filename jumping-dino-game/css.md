```css
html {
  height: 100%;
  width: 100%;
  background-color: #ebebeb;
}

#game {
  width: 500px;
  height: 200px;
  border: 1px solid black;
  margin: auto;
  background-color: white;
}

#dino {
  width: 40px;
  height: 50px;
  background-color: rgb(251, 250, 250);
  position: relative;
  top: 150px;
}

#dino img {
  margin-top: 20px;
  max-width: 100%;
  max-height: 500%;
}

@keyframes jump {
  0% {
    top: 150px;
  }

  30% {
    top: 100px;
  }

  70% {
    top: 100px;
  }

  100% {
    top: 150px;
  }
}

.animate {
  animation: jump 300ms linear;
}

#bomb {
  width: 20px;
  height: 20px;
  background-color: rgb(6, 6, 6);
  position: relative;
  border-radius: 100%;
  top: 130px;
  left: 480px;
  animation: bomb 1.6s infinite linear;
}

#bomb img {
  max-width: 100%;
  max-height: 100%;
}

@keyframes bomb {
  0% {
    left: 500px;
  }

  100% {
    left: -20px;
  }
}

#startButton,
#tryAgainButton {
  background-color: #448d44;
  border: 1px solid black;
  border-radius: 10px;
  color: white;
  font-size: 30px;
  padding: 15px;
  box-shadow: 5px 7px #7d7d7d;
  cursor: pointer;
}

#tryAgainButton {
  background-color: #f7d65f;
  color: black;
}
```
