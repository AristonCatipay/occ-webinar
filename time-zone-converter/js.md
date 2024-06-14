```javascript
// Get the necessary DOM elements
const inputTime = document.getElementById("inputTime");
const inputTimezone = document.getElementById("inputTimezone");
const outputTimezone = document.getElementById("outputTimezone");
const convertButton = document.getElementById("convertButton");
const outputTime = document.getElementById("outputTime");

// Function to convert time
const convertTime = () => {
  const inputDate = new Date(inputTime.value);
  const fromOffset = parseInt(inputTimezone.value);
  const toOffset = parseInt(outputTimezone.value);

  if (!inputDate || isNaN(fromOffset) || isNaN(toOffset)) {
    outputTime.textContent = "Please select valid time and timezones.";
    return;
  }

  // Convert the input date to UTC
  const utcDate = new Date(inputDate.getTime() + fromOffset * 60 * 60 * 1000);

  // Convert UTC date to the target timezone
  const targetDate = new Date(utcDate.getTime() + toOffset * 60 * 60 * 1000);

  // Format the target date
  const formattedDate = targetDate.toLocaleString();

  // Display the converted time
  outputTime.textContent = formattedDate;
};

// Attach event listener
convertButton.addEventListener("click", convertTime);
```
