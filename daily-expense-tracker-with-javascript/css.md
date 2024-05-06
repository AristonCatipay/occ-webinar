```css
/* Reset some default browser styles */
h1,
ul {
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  margin: 5% 15%;
}

.container {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
}

h1 {
  text-align: center;
  margin-bottom: 20px;
}

#expense-form {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}

#expense-name,
#expense-amount {
  padding: 8px;
  width: 40%;
}

#add-expense {
  padding: 8px 16px;
  background-color: #007bff;
  color: white;
  border: none;
  cursor: pointer;
  font-weight: bolder;
}

#add-expense:hover {
  background-color: #0056b3;
}

#expense-list {
  list-style-type: none;
  padding: 0;
}

.expense-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #ffffff;
  padding: 8px;
  margin-bottom: 8px;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.delete-btn {
  color: #ff0000;
  cursor: pointer;
}

.delete-btn:hover {
  text-decoration: underline;
}

#total-expense {
  text-align: center;
  font-weight: bold;
  margin-top: 20px;
}
```
