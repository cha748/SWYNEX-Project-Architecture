# SpendWise - Architecture Document

## 1. Product Idea
SpendWise is a simple web app where users record daily expenses, group them by category, and view monthly totals.

## 2. Data Models

### User
- id (ObjectId)
- name (String)
- email (String, unique)
- password (String, hashed)

### Expense
- id (ObjectId)
- userId (ObjectId, ref User)
- title (String)
- amount (Number)
- category (Food, Travel, Bills, Shopping, Other)
- date (Date)

## 3. API Routes

### Auth
- POST /api/auth/register - create account
- POST /api/auth/login - login

### Expenses
- GET /api/expenses - list all expenses
- POST /api/expenses - add an expense
- PUT /api/expenses/:id - edit an expense
- DELETE /api/expenses/:id - delete an expense
- GET /api/expenses/summary - monthly total by category

## 4. Frontend Screens
1. Register
2. Login
3. Dashboard (monthly total and category summary)
4. Add Expense
5. Expense List

## 5. Tech Stack
- Frontend: React
- Backend: Node.js + Express
- Database: MongoDB
