# Vision & Scope — QR Food System

---

## Vision

The goal of the system is to automate student meal payments at the university cafeteria using QR codes. Instead of manual paper records and cash payments, students pay instantly by showing a QR code from their mobile app. Cooks process orders in 3 clicks. Accountants generate monthly reports automatically.

The system solves a real problem — currently only 10–15 students use the cafeteria daily because the process is inconvenient. After implementation the goal is to grow this number to 50+ daily users.

---

## System Components

The system consists of two parts:

| Component | Users | Purpose |
|-----------|-------|---------|
| Mobile app | Student | View profile, balance, transaction history, show QR code for payment |
| Web interface | Cook, Accountant, Administrator | Process orders, generate reports, manage products |

---

## Scope

### What is included in this version

| # | Feature | Component |
|---|---------|-----------|
| 1 | Student profile — name, group, photo | Mobile app |
| 2 | Balance display | Mobile app |
| 3 | Transaction history with details | Mobile app |
| 4 | QR code display for payment | Mobile app |
| 5 | QR code scan and student identification | Web interface |
| 6 | Menu selection and order creation | Web interface |
| 7 | Balance check before payment | Web interface |
| 8 | Automatic balance deduction after confirmation | Web interface |
| 9 | Monthly report generation | Web interface |
| 10 | CSV export of reports | Web interface |
| 11 | Admin panel for managing products and prices | Web interface |

### What is NOT included in this version

| # | Feature | Reason |
|---|---------|--------|
| 1 | Online balance top-up | Requires payment gateway integration — planned for next version |
| 2 | Student self-service ordering | Current process requires cook to confirm orders |
| 3 | Push notifications about low balance | Planned for next version |

---

## Future Improvements

In future versions the system could include:
- Online balance top-up by students or parents
- Push notifications about low balance
- Student self-service ordering without cook involvement
