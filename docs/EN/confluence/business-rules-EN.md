# Business Rules — QR Food System

---

### BR-01 — Balance cannot be negative

The student balance cannot go below zero. If the order total is greater than the current balance, the system blocks the transaction and displays an error message: "Insufficient funds". The order is not created and the balance is not changed.

---

### BR-02 — Balance updates only after confirmation

The student balance is deducted only after the cook confirms the order. If the cook cancels before confirmation, no money is deducted and the balance stays the same.

---

### BR-03 — Transaction must contain all required data

Every transaction must include: student ID, list of ordered items, total amount, date and time. A transaction without this data cannot be saved in the system.

---

### BR-04 — Cook cannot edit balance

The cook has no permission to manually change the student balance. The balance is managed by the university scholarship system. Manual editing would violate financial rules and could lead to abuse.

---

### BR-05 — Inactive student cannot order

A student who is not registered or is marked as inactive in the system cannot place an order. The system will display an error message when scanning the QR code of an inactive student.
