```html
<div class="container">
  <h1>Timezone Converter</h1>
  <div>
    <label for="inputTime">Input Time:</label>
    <input type="datetime-local" id="inputTime" />
  </div>
  <div>
    <label for="inputTimezone">From:</label>
    <select id="inputTimezone">
      <option value="-5">New York (GMT-5)</option>
      <option value="0">London (GMT+0)</option>
      <option value="1">Berlin (GMT+1)</option>
      <option value="9">Tokyo (GMT+9)</option>
      <option value="10">Sydney (GMT+10)</option>
    </select>
  </div>
  <div>
    <label for="outputTimezone">To:</label>
    <select id="outputTimezone">
      <option value="-5">New York (GMT-5)</option>
      <option value="0">London (GMT+0)</option>
      <option value="1">Berlin (GMT+1)</option>
      <option value="9">Tokyo (GMT+9)</option>
      <option value="10">Sydney (GMT+10)</option>
    </select>
  </div>
  <button id="convertButton">Convert</button>
  <div>
    <h2>Converted Time:</h2>
    <p id="outputTime"></p>
  </div>
</div>
```
