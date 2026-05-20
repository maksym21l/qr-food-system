# System Overview — QR Food System

---

## What the System Does

The QR Food System automates student meal payments at the university cafeteria. Instead of manual paper records and cash payments, the system uses QR codes for fast student identification and digital transactions.

---

## System Components

| Component | Description |
|-----------|-------------|
| Mobile app | Used by the student — shows profile, balance, transaction history and QR code |
| Web interface | Used by cook, accountant and administrator |
| Database (PostgreSQL) | Stores all students, orders, transactions and reports |
| QR code system | Unique QR code assigned to each student for identification |

---

## How the System Works — Step by Step

### Normal flow (sufficient balance)

1. Student opens mobile app and shows QR code at the counter
2. Cook scans the QR code using the web interface
3. System finds the student and displays profile — name, group, balance
4. Student tells the cook what they want to order
5. Cook selects meals and quantity on the website
6. System automatically calculates total price
7. Cook clicks "Confirm order"
8. System checks student balance
9. Balance is sufficient — system deducts money from student account
10. Cook gives food to the student
11. Student sees updated balance in mobile app

### Alternative flow (insufficient balance)

1–7. Same steps as above
8. System checks student balance
9. Balance is NOT sufficient — system displays error message: "Insufficient funds"
10. Cook asks student what they want to remove from the order
11. Student decides — modify order or cancel
12. No money is deducted if order is cancelled

---

## Users

| User | Interface | Main Action |
|------|-----------|-------------|
| Student | Mobile app | Show QR code, view balance and history |
| Cook | Web interface | Scan QR, create order, confirm payment |
| Accountant | Web interface | Generate and export monthly reports |
| Administrator | Web interface | Manage products, prices and user accounts |
