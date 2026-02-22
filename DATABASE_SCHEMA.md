# Database Schema Design

## 1. Users
- **user_id** (INT, Primary Key)
- **username** (VARCHAR, Unique)
- **password** (VARCHAR)
- **email** (VARCHAR, Unique)
- **role** (ENUM: 'admin', 'clinic', 'assistant')
- **created_at** (DATETIME)
- **updated_at** (DATETIME)

## 2. Clinics
- **clinic_id** (INT, Primary Key)
- **clinic_name** (VARCHAR)
- **address** (VARCHAR)
- **phone_number** (VARCHAR)
- **created_at** (DATETIME)
- **updated_at** (DATETIME)

## 3. Assistants
- **assistant_id** (INT, Primary Key)
- **user_id** (INT, Foreign Key referencing Users)
- **clinic_id** (INT, Foreign Key referencing Clinics)
- **specialty** (VARCHAR)
- **created_at** (DATETIME)
- **updated_at** (DATETIME)

## 4. Time Records
- **time_record_id** (INT, Primary Key)
- **assistant_id** (INT, Foreign Key referencing Assistants)
- **date** (DATE)
- **hours_worked** (DECIMAL)
- **created_at** (DATETIME)
- **updated_at** (DATETIME)

## 5. Salary Data
- **salary_id** (INT, Primary Key)
- **assistant_id** (INT, Foreign Key referencing Assistants)
- **amount** (DECIMAL)
- **payment_date** (DATETIME)
- **created_at** (DATETIME)
- **updated_at** (DATETIME)