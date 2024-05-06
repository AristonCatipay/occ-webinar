```js
// Initialize total expense
let totalExpense = 0;

// Function to update the total expense display
function updateTotalExpense() {
  document.getElementById("total-expense").textContent =
    "Total Expense: $" + totalExpense + ".00";
}

// Function to add a new expense
function addExpense() {
  let expenseName = document.getElementById("expense-name").value;
  let expenseAmount = document.getElementById("expense-amount").value;

  if (expenseName === "" || expenseAmount === "") {
    alert("Please enter both expense name and amount.");
    return;
  }

  let expenseItem = document.createElement("li");
  expenseItem.className = "expense-item";

  let expenseInfo = document.createElement("span");
  expenseInfo.textContent = expenseName + ": $" + expenseAmount + ".00";

  let deleteButton = document.createElement("span");
  deleteButton.className = "delete-btn";
  deleteButton.textContent = "Delete";
  deleteButton.addEventListener("click", function () {
    // Subtract the deleted expense from the total
    totalExpense -= parseFloat(expenseAmount);
    updateTotalExpense();

    expenseItem.remove();

    // Update expenses in local storage
    var expenses = JSON.parse(localStorage.getItem("expenses")) || [];
    expenses = expenses.filter(function (expense) {
      return expense.name !== expenseName && expense.amount !== expenseAmount;
    });
    localStorage.setItem("expenses", JSON.stringify(expenses));
  });

  expenseItem.appendChild(expenseInfo);
  expenseItem.appendChild(deleteButton);

  document.getElementById("expense-list").appendChild(expenseItem);

  // Update the total expense
  totalExpense += parseFloat(expenseAmount);
  updateTotalExpense();

  document.getElementById("expense-name").value = "";
  document.getElementById("expense-amount").value = "";

  // Update expenses in local storage
  let expenses = JSON.parse(localStorage.getItem("expenses")) || [];
  expenses.push({ name: expenseName, amount: expenseAmount });
  localStorage.setItem("expenses", JSON.stringify(expenses));

  document.getElementById("expense-name").value = "";
  document.getElementById("expense-amount").value = "";
}

// Load expenses from local storage on page load
window.addEventListener("load", function () {
  var expenses = JSON.parse(localStorage.getItem("expenses")) || [];

  expenses.forEach(function (expense) {
    var expenseItem = document.createElement("li");
    expenseItem.className = "expense-item";

    var expenseInfo = document.createElement("span");
    expenseInfo.textContent = expense.name + ": $" + expense.amount + ".00";

    var deleteButton = document.createElement("span");
    deleteButton.className = "delete-btn";
    deleteButton.textContent = "Delete";
    deleteButton.addEventListener("click", function () {
      // Subtract the deleted expense from the total
      totalExpense -= parseFloat(expense.amount);
      updateTotalExpense();

      expenseItem.remove();

      // Update expenses in local storage
      var expenses = JSON.parse(localStorage.getItem("expenses")) || [];
      expenses = expenses.filter(function (exp) {
        return exp.name !== expense.name && exp.amount !== expense.amount;
      });
      localStorage.setItem("expenses", JSON.stringify(expenses));
    });

    expenseItem.appendChild(expenseInfo);
    expenseItem.appendChild(deleteButton);

    document.getElementById("expense-list").appendChild(expenseItem);

    // Update the total expense
    totalExpense += parseFloat(expense.amount);
    updateTotalExpense();
  });
});

// Add event listener to the "Add Expense" button
document.getElementById("add-expense").addEventListener("click", addExpense);
```
