# Data Model

## Entities
- Student
- Product
- Transaction
- MonthlyReport

## Student
Поля:
- id
- first_name
- last_name
- group
- balance

## Product
Поля:
- id
- name
- price
- category

## Transaction
Поля:
- id
- student_id
- product_id
- product_quantity
- total_price
- created_at

## MonthlyReport
Поля:
- id
- month
- year
- generated_file_path
