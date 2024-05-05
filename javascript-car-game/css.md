```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-size: 0;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-image: radial-gradient(
    circle,
    #84afcb,
    #6c98b6,
    #5581a1,
    #3f6a8c,
    #275578
  );
  font-family: Helvetica, sans-serif;
}

#game {
  margin: auto;
  padding: 20px;
  background-color: gray;
  border-radius: 20px;
  background-color: #385e79;
  border: 3px solid #cfecff;
  box-shadow: #10202c 0px 10px 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

p {
  text-align: center;
  font-size: 20px;
  color: white;
}

span {
  font-size: 20px;
  font-weight: 600;
}

#cp {
  color: lightgreen;
}

#p1 {
  color: lightskyblue;
}

#track_container {
  margin: 20px;
}

.track {
  position: static;
  display: block;
  background: rgb(68, 68, 68);
  border-right: 5px solid red;
}

#computer_track {
  border-bottom: 2px dashed yellow; /* Adjusted border-bottom with wider gap */
  border-top: 2px solid white;
}

#player_track {
  border-bottom: 2px solid white;
}

.path {
  display: inline-block;
  position: relative;
  width: 40px;
  height: 40px;
  background-color: transparent;
}

.car {
  z-index: 1;
  position: absolute;
  width: 40px;
  height: 40px;
}

#player1 {
  background: url("https://i.imgur.com/2U9AV1G.png");
  background-size: cover;
}
#computer {
  background: url("https://i.imgur.com/Cfu2wBc.png");
  background-size: cover;
}

.display {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.buttons {
  display: flex;
  width: 50%;
  justify-content: space-between;
}

button {
  padding: 10px 20px;
  font-size: 20px;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  transition: background-color 0.3s, box-shadow 0.3s;
  font-family: Helvetica, sans-serif;
  font-weight: 600;
}

#race_button {
  background-color: #6c98b6;
}

#race_button:hover {
  background-color: #5581a1;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}

#race_button:active {
  background-color: #3f6a8c;
  box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.3);
}

#reset_button {
  background-color: #e74c3c;
}

#reset_button:hover {
  background-color: #d53a2b;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}

#reset_button:active {
  background-color: #c1291a;
  box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.3);
}

#race_button:disabled,
#reset_button:disabled {
  background-color: #a0aec0;
  cursor: not-allowed;
}

.result {
  margin-top: 20px;
  font-size: 25px;
  color: white;
}
```
