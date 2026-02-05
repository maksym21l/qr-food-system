# 🍽 QR Food System

Pet-project для автоматизації обліку харчування студентів через QR-коди.

Система дозволяє швидко оплачувати страви, зберігати історію транзакцій та формувати звіти для бухгалтерії.

---

## 🚀 Features
- QR авторизація студентів
- Списання коштів з балансу
- Історія транзакцій
- Панель кухаря для вибору страв
- Адмінка для керування цінами
- Генерація звітів

---

## 🛠 Tech Stack
- Python (Flask)
- SQLite
- HTML/CSS/Bootstrap
- JavaScript
- QR-code library

---

## ▶ Run locally

```bash
git clone https://github.com/maksym21l/qr-food-system.git
cd qr-food-system

python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt
flask run
```

Open: http://127.0.0.1:5000

---

## 📊 Actors

| Actor | Role |
|-------|------|
| Student | scans QR, pays, checks balance |
| Cook | selects meals, confirms payment |
| Accountant | downloads reports |
| Admin | manages system |

---

## 📐 Diagrams
- UML
- ERD
- BPMN
- Wireframes

---

## 📸 Screenshots
(тут можна вставити картинки з docs/diagrams/wireframes)

---

## 🎯 Goal
Reduce queues, automate accounting and simplify payments in school canteens.
