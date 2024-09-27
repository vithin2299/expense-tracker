          <!DOCTYPE html>
          <html lang="en">
          <head>
              <meta charset="UTF-8">
              <meta name="viewport" content="width=device-width, initial-scale=1.0">
              <title>Expense Tracker with Custom Password</title>
              <style>
                  body {
                      font-family: 'Poppins', sans-serif;
                      background-image: url('https://images.unsplash.com/photo-1517423440428-a5a00ad493e8');
                      background-size: cover;
                      background-position: center;
                      color: white;
                      display: flex;
                      justify-content: center;
                      align-items: center;
                      height: 100vh;
                      margin: 0;
                      flex-direction: column;
                      backdrop-filter: blur(5px);
                  }

                  .tracker-card, .login-card {
                      background: rgba(0, 0, 0, 0.7);
                      border-radius: 20px;
                      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
                      padding: 30px;
                      max-width: 450px;
                      width: 100%;
                      text-align: center;
                      margin-bottom: 20px;
                      backdrop-filter: blur(5px);
                  }

                  h2 {
                      font-size: 2.5em;
                      color: #f39c12;
                      margin-bottom: 20px;
                  }

                  .input-group {
                      margin: 20px 0;
                  }

                  input {
                      width: 100%;
                      padding: 10px;
                      margin: 10px 0;
                      border: none;
                      border-radius: 10px;
                      font-size: 1.1em;
                      outline: none;
                  }

                  button {
                      background-color: #f39c12;
                      border: none;
                      color: white;
                      padding: 10px 20px;
                      font-size: 1.1em;
                      border-radius: 10px;
                      cursor: pointer;
                      transition: background-color 0.3s ease;
                  }

                  button:hover {
                      background-color: #e67e22;
                  }

                  ul {
                      list-style-type: none;
                      padding: 0;
                  }

                  ul li {
                      padding: 10px;
                      border-bottom: 1px solid rgba(255, 255, 255, 0.2);
                  }

                  h3 {
                      margin-top: 20px;
                      color: #e67e22;
                  }

                  #totalAmount, #remainingSavings {
                      font-size: 2.5em;
                      font-weight: bold;
                      color: #f1c40f;
                  }

                  #pieChartContainer {
                      width: 300px;
                      height: 300px;
                      margin-top: 20px;
                  }

              </style>
              <!-- Chart.js CDN -->
              <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
          </head>
          <body>

              <!-- Login Page -->
              <div class="login-card" id="loginCard">
                  <h2>Login or Set Password</h2>
                  <div class="input-group">
                      <input type="text" id="username" placeholder="Username" required>
                      <input type="password" id="password" placeholder="Password" required>
                      <button onclick="login()">Login/Set Password</button>
                  </div>
              </div>

              <!-- Expense Tracker Page -->
              <div class="tracker-card" id="expenseCard" style="display:none;">
                  <h2>Beautiful Expense Tracker</h2>

                  <div class="input-group">
                      <input type="text" id="description" placeholder="Expense Description">
                      <input type="number" id="amount" placeholder="Expense Amount">
                      <button onclick="addExpense()">Add Expense</button>
                  </div>

                  <div class="input-group">
                      <input type="number" id="addSavings" placeholder="Add Monthly Savings">
                      <input type="number" id="addInvested" placeholder="Add Monthly Investments">
                      <button onclick="updateSavingsInvestments()">Update Savings/Investments</button>
                  </div>

                  <h3>Expenses</h3>
                  <ul id="expenseList"></ul>

                  <h3>Total Expenses: $<span id="totalAmount">0</span></h3>
                  <h3>Remaining Savings: $<span id="remainingSavings">0</span></h3>
              </div>

              <!-- Pie Chart Container -->
              <div id="pieChartContainer" style="display:none;">
                  <canvas id="pieChart"></canvas>
              </div>

              <script>
                  let total = 0;
                  let invested = 0;
                  let savings = 0;

                  // Store credentials
                  let storedUsername = localStorage.getItem('username');
                  let storedPassword = localStorage.getItem('password');

                  // Store persistent savings and investments
                  let storedSavings = parseFloat(localStorage.getItem('savings')) || 0;
                  let storedInvested = parseFloat(localStorage.getItem('invested')) || 0;

                  // Pie chart initialization
                  const ctx = document.getElementById('pieChart').getContext('2d');
                  let pieChart = new Chart(ctx, {
                      type: 'pie',
                      data: {
                          labels: ['Expenses', 'Invested', 'Savings'],
                          datasets: [{
                              data: [0, 0, 0],
                              backgroundColor: ['#e74c3c', '#8e44ad', '#3498db'],
                              hoverOffset: 4
                          }]
                      },
                      options: {
                          responsive: true,
                          maintainAspectRatio: false,
                          plugins: {
                              legend: {
                                  labels: {
                                      color: 'white',
                                      font: {
                                          size: 16
                                      }
                                  }
                              }
                          }
                      }
                  });

                  // Add expense function
                  function addExpense() {
                      const description = document.getElementById('description').value;
                      const amount = parseFloat(document.getElementById('amount').value);

                      if (description && !isNaN(amount)) {
                          // Add expense to the list
                          const listItem = document.createElement('li');
                          listItem.textContent = `${description}: $${amount}`;
                          document.getElementById('expenseList').appendChild(listItem);

                          // Update total expenses
                          total += amount;
                          document.getElementById('totalAmount').textContent = total.toFixed(2);

                          // Update remaining savings
                          const remaining = Math.max(storedSavings - total, 0);
                          document.getElementById('remainingSavings').textContent = remaining.toFixed(2);

                          // Update the pie chart
                          updatePieChart();
                      } else {
                          alert('Please enter valid values for description and amount.');
                      }
                  }

                  // Update pie chart function
                  function updatePieChart() {
                      pieChart.data.datasets[0].data = [total, storedInvested, storedSavings];
                      pieChart.update();
                  }

                  // Login function
                  function login() {
                      const username = document.getElementById('username').value;
                      const password = document.getElementById('password').value;

                      if (!storedUsername || !storedPassword) {
                          // Set username and password if they don't exist
                          localStorage.setItem('username', username);
                          localStorage.setItem('password', password);
                          storedUsername = username;
                          storedPassword = password;
                          alert('Username and password set successfully! You can now log in.');
                          showExpenseTracker();
                      } else if (username === storedUsername && password === storedPassword) {
                          // Login if credentials match
                          showExpenseTracker();
                      } else {
                          alert("Incorrect username or password. Try again.");
                      }
                  }

                  // Show expense tracker after login
                  function showExpenseTracker() {
                      document.getElementById('loginCard').style.display = "none";
                      document.getElementById('expenseCard').style.display = "block";
                      document.getElementById('pieChartContainer').style.display = "block";
                      document.getElementById('remainingSavings').textContent = storedSavings.toFixed(2);
                      document.getElementById('totalAmount').textContent = total.toFixed(2);
                  }

                  // Update savings and investments
                  function updateSavingsInvestments() {
                      const addSavings = parseFloat(document.getElementById('addSavings').value) || 0;
                      const addInvested = parseFloat(document.getElementById('addInvested').value) || 0;

                      storedSavings += addSavings;
                      storedInvested += addInvested;

                      // Store updated values in localStorage
                      localStorage.setItem('savings', storedSavings);
                      localStorage.setItem('invested', storedInvested);

                      // Update UI
                      document.getElementById('remainingSavings').textContent = storedSavings.toFixed(2);
                      updatePieChart();

                      // Clear input fields
                      document.getElementById('addSavings').value = '';
                      document.getElementById('addInvested').value = '';
                  }

              </script>

          </body>
          </html>
