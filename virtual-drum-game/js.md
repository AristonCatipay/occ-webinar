```js
const crashRide = document.getElementById("crash-ride");
const hiHatTop = document.getElementById("hihat-top");

function animateCrashOrRide() {
  crashRide.style.transform = "rotate(0deg) scale(1.5)";
}

function animateHiHatClosed() {
  hiHatTop.style.top = "171px";
}

function playSound(e) {
  const keyCode = e.keyCode;
  const keyElement = document.querySelector(`div[data-key="${keyCode}"]`);

  if (!keyElement) return;

  const audioElement = document.querySelector(`audio[data-key="${keyCode}"]`);
  audioElement.currentTime = 0;
  audioElement.play();

  switch (keyCode) {
    case 69:
    case 82:
      animateCrashOrRide();
      break;
    case 75:
      animateHiHatClosed();
      break;
  }
}

function removeCrashRideTransition(e) {
  if (e.propertyName !== "transform") return;

  e.target.style.transform = "rotate(-7.2deg) scale(1.5)";
}

function removeHiHatTopTransition(e) {
  if (e.propertyName !== "top") return;

  e.target.style.top = "166px";
}

function removeKeyTransition(e) {
  if (e.propertyName !== "transform") return;
}

const drumKeys = Array.from(document.querySelectorAll(".key"));

drumKeys.forEach((key) => {
  key.addEventListener("transitionend", removeKeyTransition);
});

crashRide.addEventListener("transitionend", removeCrashRideTransition);
hiHatTop.addEventListener("transitionend", removeHiHatTopTransition);

window.addEventListener("keydown", playSound);
```