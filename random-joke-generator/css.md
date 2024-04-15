```css
body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
    padding: 0;
    height: 100vh;
    background: linear-gradient(to bottom, #87cefa, #008080);
}

h1 {
    margin-top: 20px;
    color: #004c4c;
}

#joke-container {
    margin-top: 30px;
    max-width: 500px;
    width: 80%;
    margin-left: auto;
    margin-right: auto;
    padding: 20px;
    border-radius: 10px;
    background-color: white;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

#joke-text {
    font-size: 18px;
    margin-top: 10px;
    padding: 10px;
    border: 2px solid #008080;
    border-radius: 10px;
    max-width: 100%;
    height: 150px;
    overflow: auto;
    background-color: #d0eafa;
    color: black;
    display: flex;
    justify-content: center;
    align-items: center;
}

#generate-button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #008080;
    color: white;
    border: none;
    border-radius: 20px;
    cursor: pointer;
    transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
}

#generate-button:hover {
    background-color: #006666;
}

#generate-button:active {
    transform: scale(0.95);
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}
```