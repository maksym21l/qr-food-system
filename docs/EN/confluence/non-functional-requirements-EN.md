# Non-Functional Requirements — QR Food System

---

### NFR-01 — Performance

**Requirement:** Every transaction must complete in 1 second or less.

**Why:** The cafeteria serves students during a short lunch break. If payment takes too long, queues form and students are late for class. Fast processing is critical for the system to be useful in a real cafeteria environment.

---

### NFR-02 — Reliability

**Requirement:** System uptime must be 95% or higher.

**Why:** If the system is unavailable during lunch hours, the cafeteria cannot serve students at all. 95% uptime means the system can be down no more than 1.2 hours per day on average. The cafeteria depends entirely on the system working during peak hours.

---

### NFR-03 — Security

**Requirement:** All users must authenticate before accessing the system. Student balance and transaction data must not be accessible to unauthorized users.

**Why:** Student balance is financial data connected to the university scholarship system. Unauthorized access could lead to data manipulation or abuse.

---

### NFR-04 — Scalability

**Requirement:** The system must support 300–500 transactions per day.

**Why:** The university has many students. During peak lunch hours multiple cooks may process orders simultaneously. The system must handle this load without slowing down or crashing.

---

### NFR-05 — Usability

**Requirement:** The cook must be able to complete a full order in 3 clicks or less.

**Why:** More clicks means more time per student. With 3 clicks the cook can serve students quickly, the queue moves faster, and students are not late for class. If the interface required 10 clicks, the cook could get confused, make mistakes, and the whole process would slow down significantly. The system must be simple enough to use without training.
