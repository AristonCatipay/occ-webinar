```css
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Architects+Daughter&family=Indie+Flower&display=swap");

* {
  margin: 10px;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Poppins", sans-serif;
  text-align: center;
  min-height: 100vh;
}

h1 {
  font-family: "Architects Daughter", cursive;
  font-weight: bold;
  font-size: 60px;
  letter-spacing: 2px;
  text-shadow: 6px 3px 8px white;
}

.main-container {
  margin: 50px;
  border: 3px solid #ecdccd;
  border-radius: 50px;
  background-color: #fee6e6;
  background-image: url("https://i.pinimg.com/736x/32/cf/72/32cf723c4e9e28e24ad3c622065dbd51.jpg");
  background-size: contain;
  background-position: left bottom;
  background-repeat: no-repeat;
}

#game-container {
  position: relative;
  width: 300px;
  height: 300px;
  margin: 20px auto;
  border: 2px dashed white;
  border-radius: 10px;
  background-color: #f0f0f0;
}

#cat {
  position: absolute;
  width: 100px;
  height: 100px;
  cursor: crosshair;
}

#score {
  margin: 10px;
  padding: 5px;
  border-radius: 5px;
  border-bottom: 2px solid;
  background: #faf2d9;
  color: #5c4600;
  font-size: 24px;
  font-weight: 500;
}

#timer {
  font-size: 24px;
  margin-bottom: 10px;
}

#start-button,
#reset-button {
  padding: 12px;
  border: 3px outset #e7e7e7;
  border-radius: 30px;
  font-size: 15px;
  font-weight: 500;
  background-color: #a4d68c;
  color: black;
}

#start-button:hover {
  background-color: green;
  color: white;
  font-weight: bold;
  cursor: pointer;
}

#reset-button {
  background-color: #ffe590;
}

#reset-button:hover {
  background-color: #ebbd23;
  color: black;
  font-weight: bold;
  cursor: pointer;
}

.bottom-container {
  display: flex;
  align-items: center;
  justify-content: center;
}
```
