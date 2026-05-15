# User Stories & Acceptance Criteria

---

# Authentication & Account

## US-01 Login & Logout

### User Story
As a user,  
I want to be able to log in and log out,  
so that I can securely access my account.

### Acceptance Criteria
- User can log in using valid student code
- System authenticates the user
- User is redirected to dashboard after successful login
- Error message is displayed if student code is invalid
- User can log out from the system
- Session is terminated after logout

---

## US-02 Simple Login Using Student Code

### User Story
As a user,  
I want a simple login using only my student code,  
so that I can quickly access the system.

### Acceptance Criteria
- Login form contains student code field
- User can enter student code
- System validates student code
- User is logged in if code is valid
- Error message is shown if code is invalid

---

## US-03 View Balance

### User Story
As a student,  
I want to see my balance,  
so that I can know how much money I have for meals.

### Acceptance Criteria
- Student can access balance page after login
- System displays current balance
- Balance is displayed in correct currency
- Balance updates after each transaction
- Unauthorized users cannot access balance page

---

# Menu & Orders

## US-04 Meal Selection

### User Story
As a student,  
I want to choose meals from the menu,  
so that I can order food quickly.

### Acceptance Criteria
- Student can view list of meals
- Each meal contains name, description, and price
- Student can select meal
- Student can confirm order
- Order is saved in the system

---

## US-05 Record Student Meals

### User Story
As a cook,  
I want to record student meals quickly,  
so that I can serve food efficiently.

### Acceptance Criteria
- Cook can select student
- Cook can select meal
- Cook can record meal
- System saves meal record
- Meal appears in student history

---

# Payments & Transactions

## US-06 QR-Code Payment

### User Story
As a student,  
I want to pay using QR-code,  
so that I can quickly complete payment.

### Acceptance Criteria
- Student can initiate payment
- System generates QR-code
- QR-code contains correct payment information
- QR-code is valid and scannable
- QR-code expires after defined time

---

## US-07 Transaction History

### User Story
As a student,  
I want to see my purchase history,  
so that I can track my transactions.

### Acceptance Criteria
- Student can open transaction history page
- System displays transaction list
- Each transaction contains date, amount, and meal information
- Transactions are sorted by date
- Student can only view personal transactions

---

# Accountant Features

## US-08 Monthly Report

### User Story
As an accountant,  
I want to generate monthly reports,  
so that I can analyze cafeteria transactions.

### Acceptance Criteria
- Accountant can select month
- System generates report for selected month
- Report contains all transactions
- Report displays totals
- Report is displayed correctly

---

## US-09 Export Report to CSV

### User Story
As an accountant,  
I want to export reports to CSV,  
so that I can use them externally.

### Acceptance Criteria
- Accountant can export report to CSV
- System generates CSV file
- CSV contains correct data
- File downloads successfully
- File opens without errors

---

## US-10 Export Report to Excel

### User Story
As an accountant,  
I want to export reports to Excel,  
so that I can use them in accounting systems.

### Acceptance Criteria
- Accountant can export report to Excel
- Excel file contains correct data
- File downloads successfully
- File opens correctly
- Exported data matches system data

---

## US-11 Filter Transactions

### User Story
As an accountant,  
I want to filter transactions by date,  
so that I can analyze specific periods.

### Acceptance Criteria
- Accountant can select date filter
- System displays filtered results
- Filter shows correct transactions
- Filter can be cleared
- Results update after filter change