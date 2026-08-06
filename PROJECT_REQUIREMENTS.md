# Smart Expense Tracker

Business Expense Management System for Small Coffee Shops

---

**Document:** Project Requirements Specification (PRS)  
**Version:** 0.1.0  
**Status:** Planning  
**Author:** Harvey Jayrell Moras  
**Repository:** smart-expense-tracker  
**Last Updated:** August 5, 2026

---

## Table of Contents

1. Project Overview
2. Vision
3. Client Background
4. Business Problem
5. Target Users
6. User Journey (MVP)
7. User Stories
8. Functional Requirements
9. Non-functional Requirements
10. Tech Stack
11. Database Design
12. Milestones / Roadmap
13. Future AI Features


## 1. Project Overview
- The application is a business expense management system 
for small coffee shop businesses that suffers from inefficient data expense handling, after using the application the user is expected to save time browsing and to easily compare monthly expenses.

## 2. Vision
- the vision of this project is to help small coffee shop business by managing expenses, organizing expenses, and monitor the expenses so that it saves time and effort into making a good financial decision resulting to improved profitability.

## 3. Success Metrics
The project will be considered as successful if:

- Expense recording takes less time than one minute.
- Monthly expense summaries are  generated instantly.
- Owner can search the expense record within seconds.
- Reduce manual receipt organization by at least 70%.

## 4. Project Scope

### lncluded in Version 1
- authentication
- expense CRUD
- Dashborad
- Expense summary

### Not Included
- ai insights
- OCR
- Forecasting
- Receipt Scanning

## 5. Client Background
- small startup coffee business that has a 3-12 employees and have a single branch on the us currently just have an excel and physical records because of the lack of accounting software and an excel is harder to navigate as the business grows.

## 6. Business Problem
- the owner spends 4-5 hours organizing receipts
- expenses are not well organized
- getting hard to track records
- hard to compare monthly expenses

because of poor expense tracking it results to late financial report making into poor decision making and ultimately reducing business profitability.

## 7. Target Users
- coffee shop owner - (Primary user)
- coffee shop manager
- cashier

## 8. user Journey (MVP)
1. User Logs into the system.
2. User views today's expenses dashboard.
3. User record new expense.
4. User search for an expense.
5. User delete and edit expense
4. User reviews the updated summary expenses.
5. User Logs out.

## 9. User Stories

### Authentication

### US-001 - Secure Login

As a coffe shop owner, 

i want to securely login to the system, 

so that only an authorized personnel can access the business records.

### US-009 - logout

As a coffee shop owner,

I want to securely logout to the system, 

so that it will be more secured and cannot be access by any people.

### Dashboard

### US-002 - Dashboard

As a coffee shop owner, 

i want to view the dashboard,

so that i can quickly monitor my business expenses


### Expense Management

### US-003 - Viewing today's expenses

As a coffe shop owner,
i want to view todays expenses,

so i can monitor my daily spending.

### US-004 - record new expenses

As a coffee shop owner,

i want to record a new expense,

so i can document all of the business expense accurately.

### US-005 - Edit an Expense

As a coffee shop owner,

i want to edit my expenses,

so i can easily replace if i mistype the amount of the expense.

### US-006 - Delete an Expense

As a coffee shop owner,

i want to delete an expense,

so that i can keep my expense records as accurate as possible.

### US-007 - Search Expenses

As a coffee shop owner,

i want to search for an expense,

so i can easily find the expense and save time finding manually.

### Reports

### US-008 - view summary expense

As a coffee shop owner, i

i want to view the summary of my expenses,

so that i can make informed financial decisions.


## 10. Functional Requirements

### FR-001 - User Login

The system shall allow registered user to log in using their email and password.

### FR-002 - Credential Validation

The system shall validate the user's credentials before granting access.

### FR-003 - Authentication Failure

The system should display an error message when invalid credentials are entered.

### FR-004 - Display Dashboard

The system shall display the dashboard after successful authentication.

### FR-005 - View Today's Expenses

The system should display today's expenses.

### FR-006 - Create Expense

The system shall allow users to create a new expense record.

### FR-007 - Edit Expense

The system shall require the following information:

* Expense Name
* Category
* Amount
* Date 
* Optional Notes

The system shall allow users to edit existing expense records.

### FR-008 - Delete Expense

The system shall allow users to delete existing expense records after confirmation.

### FR-009 - Search Expense

The system shall allow users to search expenses by keyword or category.

### FR-010 - View Expense Summary

The system shall generate a summary of recorded expenses.

### FR-011 - User Logout

The system should allow the user to have an option to logout securely.

### FR-012 - Input Validation

The system shall validate all required fields before allowing user to save the expense.

### FR-013 - Error Handling

The system shall display clear error messages when an operation cannot be completed.

## 11. Non-functional Requirements

### Performance
- The system shall load the dashboard within 2 seconds.

### Security
- Password shall be hashed using bcrypt
- Users must be authenticated before granting access.

### Reliability
- The data should be permanently stored inside the PostgreSQL database.

### Scalability
- The system shall support at least 10 concurrent users.

### Usability
- The interface shall be easy to navigate without training.

### Maintainability
- The applicaiton shall follow a modular flask project structure.


## 12. Tech Stack

Backend
- Flask

Database
- PostgreSQL (Supabase)

ORM
- SQLAlchemy

Database Migration
- Alembic

Fronted
- HTML
- CSS
- Bootstrap 5
- JavaScript

Authentication
- Flask-Login
- Werkzeug Password Hashing

Deployment
- Docker
- Render

Version Control
- Git
- Github

## 13. Database Design

The application uses a relational PostgreSQL database following a one-to-many relationship model.

### Database Entities

#### Users
- id
- name
- email
- password_hash
- role
- created_at

#### Categories
- id
- name
- description
- created_at

#### Expenses
- id
- title
- amount
- expense_date
- notes
- user_id (FK)
- category_id (FK)
- created_at
- updated_at

### Relationships

- One User can have many Expenses.
- One Category can have many Expenses.
- Every Expense belongs to one User.
- Every Expense belongs to one Category.

### ER Diagram

![ER Diagram](C:\Users\admin\Projects\smart-expense-tracker\docs\screenshots\smart-expense-tracker_db_design.png)

## 14. Milestones / Roadmap

### v0.1.0 — Planning
- Project Requirements
- User Stories
- ER Diagram

### v0.2.0 — Authentication
- Flask Setup
- User Login
- User Logout

### v0.3.0 — Expense Management
- Create Expense
- Edit Expense
- Delete Expense
- Search Expense

### v0.4.0 — Dashboard
- Dashboard
- Expense Summary

### v0.5.0 — Deployment
- Docker
- Render Deployment

### v1.0.0 — Production Release
- Stable Release

## 15. Future AI Features

Version 2 of the application may include:

- AI expense categorization
- Receipt OCR
- Spending trend analysis
- Monthly expense forecasting
- Budget recommendations
- Profit estimation
- Natural language expense search