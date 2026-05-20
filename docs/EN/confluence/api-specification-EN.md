# API Specification — QR Food System

**Version:** 1.0  
**Base URL:** `https://api.qr-food-system.com/api`  
**Format:** JSON

---

## HTTP Status Codes Used

| Code | Meaning |
|------|---------|
| 200  | OK — request successful |
| 201  | Created — new record created |
| 400  | Bad Request — wrong or missing data |
| 404  | Not Found — resource does not exist |

---

## 1. Authentication

### POST /api/auth/login

User logs into the system.

**Request:**
```json
{
  "email": "olena@school.edu",
  "password": "password123"
}
```

**Response 200:**
```json
{
  "user_id": "1",
  "email": "olena@school.edu",
  "role": "cook"
}
```

**Response 400** — missing email or password  
**Response 404** — user not found

---

## 2. Student

### GET /api/students/{qr_token}

Returns student info after QR code scan.

**Example:** `GET /api/students/QR-2024-550e8400`

**Response 200:**
```json
{
  "student_id": "1",
  "first_name": "Ivan",
  "last_name": "Petrenko",
  "group_name": "CS-21",
  "balance": 145.50
}
```

**Response 404** — student with this QR not found

---

## 3. Products

### GET /api/products

Returns the list of available meals in the cafeteria.

**Response 200:**
```json
{
  "products": [
    {
      "product_id": "1",
      "name": "Borscht",
      "price": 25.00,
      "category": "first_course"
    },
    {
      "product_id": "2",
      "name": "Cutlet with mashed potatoes",
      "price": 45.00,
      "category": "main_dish"
    }
  ]
}
```

**Response 404** — no products available

---

## 4. Orders

### POST /api/orders

Creates a new order and deducts money from student balance.

**Request:**
```json
{
  "student_id": "1",
  "items": [
    {
      "product_id": "1",
      "quantity": 1
    },
    {
      "product_id": "2",
      "quantity": 1
    }
  ]
}
```

**Response 201:**
```json
{
  "order_id": "55",
  "student_id": "1",
  "total_price": 70.00,
  "status": "completed",
  "remaining_balance": 75.50
}
```

**Response 400** — not enough balance  
**Response 404** — student or product not found

---

## 5. Reports

### GET /api/reports/monthly

Returns monthly report for the accountant.

**Example:** `GET /api/reports/monthly?month=10&year=2025`

**Response 200:**
```json
{
  "month": 10,
  "year": 2025,
  "total_transactions": 342,
  "total_revenue": 15480.00
}
```

**Response 404** — no data for this period
