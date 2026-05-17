# Use Case Specification

---

# UC-01 — Cafeteria Order Processing via Student QR Identification

| Field | Description |
|---|---|
| Use Case ID | UC-01 |
| Use Case Name | Cafeteria Order Processing via QR |
| Primary Actor | Cook |
| Secondary Actors | Student, System |
| Scope | QR Lunch Ordering System |
| Level | User Goal |

---

# 🎯 Goal

Identify the student, create a meal order, deduct funds from the student balance, and store the transaction in the system.

---

# Preconditions

- Cook is authenticated in the system
- Menu is available for ordering
- Student is registered in the database
- Student has a unique QR-code

---

# Trigger

The student scans a QR-code at the cafeteria counter, after which the system opens the student profile on the cook’s screen.

---

# Main Success Scenario

1. Student scans QR-code
2. System finds student profile
3. Student information is displayed to the cook:
   - full name
   - group
   - balance
4. Student tells desired meals to the cook
5. Cook selects meals and quantity in the web interface
6. System automatically calculates total order amount
7. Cook confirms the order
8. System validates student balance
9. System deducts funds from student account
10. System creates transaction
11. System stores transaction in database
12. System displays successful payment message
13. System updates student balance
14. Cook serves lunch to the student

---

# Postconditions

## Success Postconditions

- Transaction is stored in the system
- Student balance is updated
- Order data is available for reporting

## Failure Postconditions

- Transaction is not created
- Balance is not changed
- Operation is marked as failed or canceled

---

# Alternative Flows

## A1 — Student Not Found

1. System cannot find student
2. Message is displayed:

```text
Student not found
```

3. Process ends

---

## A2 — Insufficient Funds

1. System validates balance
2. Balance is insufficient
3. Message is displayed:

```text
Insufficient funds
```

4. Cook can:
   - modify the order
   - cancel the operation

---

## A3 — Order Cancellation

1. Cook cancels operation before confirmation
2. Order is not created
3. No funds are deducted

---

## A4 — Invalid QR-code

1. System cannot read QR-code
2. Message is displayed:

```text
Invalid QR-code
```

3. System returns user to QR scanning step

---

# Exception Flows

## E1 — Payment Processing Error

1. Payment processing error occurs
2. Transaction is not created
3. Balance is not changed
4. Error message is displayed

---

## E2 — System Unavailable

1. System becomes unavailable
2. Message is displayed:

```text
System temporarily unavailable
```

3. Process ends