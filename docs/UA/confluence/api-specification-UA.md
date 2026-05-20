# API Специфікація — QR Food System

**Версія:** 1.0  
**Базова URL:** `https://api.qr-food-system.com/api`  
**Формат:** JSON

---

## HTTP Статус-коди

| Код  | Значення |
|------|----------|
| 200  | OK — запит успішний |
| 201  | Created — новий запис створено |
| 400  | Bad Request — невірні або відсутні дані |
| 404  | Not Found — ресурс не знайдено |

---

## 1. Автентифікація

### POST /api/auth/login

Користувач входить у систему.

**Запит (Request):**
```json
{
  "email": "olena@school.edu",
  "password": "password123"
}
```

**Відповідь (Response) 200:**
```json
{
  "user_id": "1",
  "email": "olena@school.edu",
  "role": "cook"
}
```

**Response 400** — відсутній email або пароль  
**Response 404** — користувача не знайдено

---

## 2. Студент

### GET /api/students/{qr_token}

Повертає дані студента після сканування QR-коду.

**Приклад:** `GET /api/students/QR-2024-550e8400`

**Відповідь (Response) 200:**
```json
{
  "student_id": "1",
  "first_name": "Іван",
  "last_name": "Петренко",
  "group_name": "CS-21",
  "balance": 145.50
}
```

**Response 404** — студента з таким QR не знайдено

---

## 3. Продукти

### GET /api/products

Повертає список доступних страв у їдальні.

**Відповідь (Response) 200:**
```json
{
  "products": [
    {
      "product_id": "1",
      "name": "Борщ",
      "price": 25.00,
      "category": "перша страва"
    },
    {
      "product_id": "2",
      "name": "Котлета з пюре",
      "price": 45.00,
      "category": "друга страва"
    }
  ]
}
```

**Response 404** — продуктів немає

---

## 4. Замовлення

### POST /api/orders

Створює нове замовлення та списує кошти з балансу студента.

**Запит (Request):**
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

**Відповідь (Response) 201:**
```json
{
  "order_id": "55",
  "student_id": "1",
  "total_price": 70.00,
  "status": "completed",
  "remaining_balance": 75.50
}
```

**Response 400** — недостатньо коштів на балансі  
**Response 404** — студента або продукт не знайдено

---

## 5. Звіти

### GET /api/reports/monthly

Повертає місячний звіт для бухгалтера.

**Приклад:** `GET /api/reports/monthly?month=10&year=2025`

**Відповідь (Response) 200:**
```json
{
  "month": 10,
  "year": 2025,
  "total_transactions": 342,
  "total_revenue": 15480.00
}
```

**Response 404** — даних за цей період немає
