```css
.main-title {
	font-family: 'Pacifico', cursive;
	text-align: center;
	font-size: 50px;
	color: #cb2026;
}

.drum-kit-wrapper {
	position: relative;
	width: 600px;
	margin: -100px auto 0;
}


#crash-ride {
	position: absolute;
	top: 114px;
  left: 80px;
  transform: rotate(-7.2deg) scale(1.5);
  transition: all ease-in-out .042s;
}

#hihat-top {
	position: absolute;
  top: 166px;
  right: 71px;
  transform: scale(1.35);
  z-index: 0;
  transition: all ease-in-out .042s;
}

.drum-kit {
	width: 100%;
	height: 520px;
	position: relative;
}

.key {
	display: inline-block;
	transition: all ease-in-out .042s;
	position: absolute;
	background: #eaeaea;
  font-size: 1.5em;
  height: 32px;
  width: 32px;
  text-align: center;
  border-radius: 4px;
  border: 3px solid #aaa;
  z-index: 2;
}

#kick {
	top: 355px;
  right: 250px;
}

#kick2 {
  top: 355px;
  right: 308px;
}

#snare {
	right: 145px;
  top: 280px;
}

#tom-high {
	right: 227px;
  top: 240px;
}

#tom-mid {
	left: 222px;
  top: 220px;
}

#tom-low {
	top: 320px;
  left: 133px;
}

#crash {
	top: 80px;
  left: 75px;
}

#ride {
	left: 165px;
  top: 87px;
}

#hihat-open {
	right: 165px;
  top: 144px;
}

#hihat-close {
	right: 60px;
  top: 150px;
}
```