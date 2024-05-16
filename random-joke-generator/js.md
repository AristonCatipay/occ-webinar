```js
const jokes = [
  "Why don't programmers like nature? It has too many bugs.",
  "Why did the computer go to the doctor? It had a virus!",
  "Why was the JavaScript developer sad? Because he didn't know how to 'null' his feelings.",
  "Why did the smartphone go to therapy? It had too many hang-ups.",
  "Why did the computer keep cold? It left its Windows open!",
  "Why was the computer cold? It left its Windows open!",
  "Why don't programmers like to go outside? The sun makes their screens go glare.",
  "Why was the math book sad? Because it had too many problems.",
  "Why was the JavaScript developer broke? Because he used up all his cache!",
  "Why was the computer cold? It left its Windows open!",
];

const jokeText = document.getElementById("joke-text");
const generateButton = document.getElementById("generate-button");

generateButton.addEventListener("click", () => {
  const randomIndex = Math.floor(Math.random() * jokes.length);
  jokeText.textContent = jokes[randomIndex];
});
```
