```js
const jokes = [
    // Your generated list of jokes from ChatGPT
];

const jokeText = document.getElementById('joke-text');
const generateButton = document.getElementById('generate-button');

generateButton.addEventListener('click', () => {
    const randomIndex = Math.floor(Math.random() * jokes.length);
    jokeText.textContent = jokes[randomIndex];
});
```