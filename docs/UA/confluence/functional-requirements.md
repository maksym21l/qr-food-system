# Functional Requirements

## 1. Authentication

### FR-01 — User Login
Система повинна дозволяти студентам та кухарям входити за допомогою унікального student code.

### Acceptance Criteria
- User enters student code
- System validates code
- User is logged in successfully
- If invalid → error message displayed

### FR-02 — User Logout
Система повинна дозволяти користувачу виходити з акаунту.

---

## 2. Student Account

### FR-03 — View Student Profile
Відображаються:
- First name
- Last name
- Group
- Balance

### FR-04 — View Balance
Rules:
- Balance is read-only
- Balance updates after transaction

### FR-05 — View Transaction History
Відображаються:
- Date
- Product name
- Quantity
- Total price

---

## 3. Menu

### FR-06 — View Menu
Відображаються:
- Product name
- Price
- Category

### FR-07 — Select Products
Rules:
- Quantity can be changed
- Total price calculated automatically

---

## 4. Transactions

### FR-08 — Create Transaction
Process:
- Check balance
- Deduct money
- Save transaction

### FR-09 — Validate Balance
If insufficient balance → transaction rejected

### FR-10 — Update Balance
Balance updates after successful transaction

---

## 5. Reports

### FR-11 — Generate Monthly Report

### FR-12 — Export Report
Supported formats:
- Excel
- PDF
