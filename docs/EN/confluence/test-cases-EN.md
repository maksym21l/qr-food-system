# Test Cases — QR Food System

---

## Authentication

### TC-AUTH-01 — Login with valid credentials

| Field | Description |
|-------|-------------|
| **ID** | TC-AUTH-01 |
| **Name** | Login with valid credentials |
| **Precondition** | User is registered in the system |

**Steps:**
1. Open login page
2. Enter valid email and password
3. Click "Login"

**Expected Result:** User is logged in and redirected to dashboard

---

### TC-AUTH-02 — Login with invalid credentials

| Field | Description |
|-------|-------------|
| **ID** | TC-AUTH-02 |
| **Name** | Login with invalid credentials |
| **Precondition** | User is on the login page |

**Steps:**
1. Open login page
2. Enter wrong email or password
3. Click "Login"

**Expected Result:** Error message is displayed. User stays on login page

---

### TC-AUTH-03 — Logout

| Field | Description |
|-------|-------------|
| **ID** | TC-AUTH-03 |
| **Name** | Logout from the system |
| **Precondition** | User is logged in |

**Steps:**
1. Click "Logout" button

**Expected Result:** Session is ended. User is redirected to login page

---

## QR Code

### TC-QR-01 — Scan valid QR code

| Field | Description |
|-------|-------------|
| **ID** | TC-QR-01 |
| **Name** | Scan valid student QR code |
| **Precondition** | Cook is logged in. Student has a valid QR code |

**Steps:**
1. Student shows QR code at the counter
2. Cook scans the QR code
3. System searches for student in the database

**Expected Result:** Student profile is displayed — name, group, balance

---

### TC-QR-02 — Scan invalid QR code

| Field | Description |
|-------|-------------|
| **ID** | TC-QR-02 |
| **Name** | Scan invalid or unreadable QR code |
| **Precondition** | Cook is logged in |

**Steps:**
1. Student shows damaged or wrong QR code
2. Cook scans the QR code
3. System cannot find student

**Expected Result:** Error message is displayed — "Invalid QR code". System returns to scan screen

---

## Transactions

### TC-TR-01 — Successful order and payment

| Field | Description |
|-------|-------------|
| **ID** | TC-TR-01 |
| **Name** | Create order with sufficient balance |
| **Precondition** | Cook is logged in. Student balance is sufficient |

**Steps:**
1. Student shows QR code
2. Cook scans QR code — student profile appears
3. Cook asks student what they want to order
4. Cook selects meals and quantity on the website
5. System calculates total price
6. Cook clicks "Confirm order"
7. System checks student balance
8. System deducts money from balance
9. Cook gives food to student

**Expected Result:** Order is created. Balance is updated. Success message is displayed

---

### TC-TR-02 — Order with insufficient balance

| Field | Description |
|-------|-------------|
| **ID** | TC-TR-02 |
| **Name** | Create order when student has not enough money |
| **Precondition** | Cook is logged in. Student balance is less than order total |

**Steps:**
1. Student shows QR code
2. Cook scans QR code — student profile appears
3. Cook selects meals
4. Cook clicks "Confirm order"
5. System checks student balance
6. Balance is not enough

**Expected Result:** Error message is displayed — "Insufficient funds". Order is not created. Balance is not changed

---

### TC-TR-03 — Balance update after payment

| Field | Description |
|-------|-------------|
| **ID** | TC-TR-03 |
| **Name** | Balance decreases after successful order |
| **Precondition** | Student has balance 100.00 UAH. Order total is 70.00 UAH |

**Steps:**
1. Cook creates and confirms order for 70.00 UAH
2. System processes payment
3. Cook or student checks balance

**Expected Result:** Balance shows 30.00 UAH

---

## Reports

### TC-REP-01 — Generate monthly report

| Field | Description |
|-------|-------------|
| **ID** | TC-REP-01 |
| **Name** | Accountant generates monthly report |
| **Precondition** | Accountant is logged in. Transactions exist for selected month |

**Steps:**
1. Accountant opens reports page
2. Selects month and year
3. Clicks "Generate report"

**Expected Result:** Report is displayed with total transactions and total revenue

---

### TC-REP-02 — Export report to CSV

| Field | Description |
|-------|-------------|
| **ID** | TC-REP-02 |
| **Name** | Accountant exports report to CSV |
| **Precondition** | Accountant is logged in. Report for selected month exists |

**Steps:**
1. Accountant opens report for selected month
2. Clicks "Export to CSV"

**Expected Result:** CSV file is downloaded successfully. File contains correct data
