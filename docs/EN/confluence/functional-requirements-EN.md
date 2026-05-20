# Functional Requirements — QR Food System

---

## Authentication

### FR-01 — User Login
The system must allow cook, accountant and administrator to log in using email and password.

### FR-02 — User Logout
The system must allow the user to log out. After logout the session is ended and user is redirected to login page.

---

## Student Account

### FR-03 — View Student Profile
After QR code scan the system must display student information — full name, group, and current balance.

### FR-04 — View Balance
The system must show the current balance of the student. Balance must update after every transaction.

### FR-05 — View Transaction History
The system must show a list of past transactions for each student — date, amount, and meal name.

---

## Menu

### FR-06 — View Menu
The system must display a list of available meals with name, price, and category.

### FR-07 — Select Products
The cook must be able to select meals and quantity from the menu when creating an order.

---

## Transactions

### FR-08 — Create Transaction
When the cook confirms an order, the system must check the student balance. If balance is sufficient — the transaction is created and money is deducted. If balance is not sufficient — an error message is displayed and the order is not created.

### FR-09 — Validate Balance
Before processing payment the system must check that student balance is greater than or equal to the order total.

### FR-10 — Update Balance
After successful payment the system must subtract the order amount from the student balance and save the new balance.

---

## Reports

### FR-11 — Generate Monthly Report
The system must allow the accountant to generate a report for a selected month and year. The report must show total number of transactions and total revenue.

### FR-12 — Export Report
The system must allow the accountant to export the monthly report as a CSV file.
