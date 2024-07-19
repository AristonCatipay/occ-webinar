```css
body {
  height: 100vh;
  background-color: #f7f7f7;
  display: flex;
  overflow: hidden;
}

.screen-output {
  background: #212331;
  width: 325px;
  border: 0;
  color: #fff;
  font-size: 68px;
  overflow: hidden;
  height: 160px;
  pointer-events: none;
  text-align: right;
  padding: 0 20px;
  border-radius: 40px 40px 0 0;
}

.calc-body {
  border-radius: 40px;
  max-width: fit-content;
  background: #212331;
  margin: auto;
  padding: 0px;
  height: auto;
  box-shadow: 0px 10px 5px 0px rgba(0, 0, 0, 0.15);
}

.button-container {
  max-width: 100%;
  grid: repeat(4, 1fr) / auto-flow;
  display: grid;
  grid-gap: 15px;
  padding: 20px;
}

.button-container button {
  height: 70px;
  margin: auto;
  background: #fff;
  border: none;
  width: 70px;
  font-size: 20px;
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.13s ease;
}

.button-container button:hover {
  opacity: 0.5;
}

.gray {
  background: #b5b5b5 !important;
}

.yellow {
  background: #f7a241 !important;
  border: none;
}
```
