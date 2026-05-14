# Data Model

## Entities
- Student
- Product
- Transaction
- MonthlyReport

## Student
- id
- first_name
- last_name
- group
- balance

## Product
- id
- name
- price
- category

## Transaction
- id
- student_id
- product_id
- product_quantity
- total_price
- created_at

## MonthlyReport
- id
- month
- year
- generated_file_path
