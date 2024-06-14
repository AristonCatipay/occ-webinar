```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f0f0f0;
}

.container {
  border-radius: 20px;
  background: #f5f5f5;
  position: relative;
  padding: 1.8rem;
  border: 2px solid #c3c6ce;
  transition: 0.5s ease-out;
  overflow: visible;
}

h1,
h2 {
  text-align: center;
}

div {
  margin-bottom: 10px;
}

label {
  margin-right: 10px;
}

select,
input,
button {
  padding: 10px;
  margin: 5px;
  border: 1px solid #ccc;
  border-radius: 3px;
  cursor: pointer;
}

#outputTime {
  font-size: 1.2em;
  font-weight: bold;
  text-align: center;
}

/* Hover */
.container:hover {
  border-color: #008bf8;
  box-shadow: 0 4px 18px 0 rgba(0, 0, 0, 0.25);
}
```
