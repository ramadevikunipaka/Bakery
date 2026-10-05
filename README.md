# Home Bakery Order Management System

A beginner-friendly full-stack PBL project based on the requirements in the assignment: Java 17+, Spring Boot backend, React frontend, REST APIs, JPA/Hibernate and MySQL.

## Features
- View bakery products
- Place an order with quantity and customization
- Delivery date, address and contact details
- Automatic total calculation
- Order confirmation
- Baker dashboard
- Update order status
- Backend validation and HTTP status codes
- MySQL persistence using JPA/Hibernate

## Architecture
React UI -> REST API -> Spring Boot Controller -> Service -> JPA Repository -> MySQL

## Requirements
- JDK 17+
- Maven 3.9+
- MySQL 8+
- Node.js 18+
- npm
- Git

## 1. Database
Create the database using `database/schema.sql`, or simply create `home_bakery` in MySQL. Spring Boot will create/update the tables with JPA.

Default local database settings are:
- database: home_bakery
- username: root
- password: root

If your MySQL password is different, set environment variables:
`DB_USERNAME` and `DB_PASSWORD`.

## 2. Run backend
Open a terminal in `backend`:

```bash
mvn spring-boot:run
```

Backend: http://localhost:8080

Useful APIs:
- GET http://localhost:8080/api/products
- POST http://localhost:8080/api/orders
- GET http://localhost:8080/api/orders
- PUT http://localhost:8080/api/orders/{id}/status

## 3. Run frontend
Open another terminal in `frontend`:

```bash
npm install
npm run dev
```

Open the URL printed by Vite, normally http://localhost:5173.

## 4. GitHub
Do not upload `backend/target`, `frontend/node_modules`, passwords, or `.env` files.

```bash
git init
git add .
git commit -m "Initial Home Bakery Order Management System"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```

## Project structure
```
HomeBakeryOrderManagement/
├── backend/
│   ├── pom.xml
│   └── src/main/java/com/homebakery/
│       ├── controller/
│       ├── dto/
│       ├── model/
│       ├── repository/
│       └── service/
├── frontend/
│   ├── package.json
│   └── src/
├── database/schema.sql
├── .gitignore
└── README.md
```

## Note
This is a PBL/learning starter project. Authentication, payment integration, production CORS configuration, image uploads and deployment configuration can be added as the next phase.
