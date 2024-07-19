```javascript
const screen = document.querySelector(".screen-output");
const buttons = document.querySelectorAll(".button-container button");
let expression = ""; // Store the current expression

buttons.forEach((button) => {
  button.addEventListener("click", () => {
    const value = button.getAttribute("value");
    if (value === "=") {
      try {
        // Evaluate the expression using the eval() function (not recommended for production use)
        expression = eval(expression).toString();
      } catch (error) {
        expression = "Error";
      }
    } else if (value === "C") {
      expression = ""; // Clear the expression
    } else {
      expression += value; // Append the clicked button value to the expression
    }
    screen.value = expression; // Update the screen with the current expression
  });
});
```
