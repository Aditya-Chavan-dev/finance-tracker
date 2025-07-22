# 💸 Finance Tracker – Real-Time Expense Intelligence

A **full-stack personal finance management tool** that enables users to track income, log expenses, and receive intelligent insights on budgeting, savings, and emergency fund planning. Built with **React**, **Node.js**, and **Microsoft SQL Server**, the project showcases secure authentication and seamless front-to-back integration.

---

## 🚀 Features

* 🔐 **User Authentication** – Login system integrated with MSSQL using parameterized queries (SQL injection safe).
* 📊 **Expense & Salary Inputs** – Modular form components to capture recurring and one-time financial entries.
* 📈 **Budget Analytics** – Visual components (coming soon) to guide decisions on spending vs. saving.
* 📁 **Environment-Secured Configuration** – All database credentials securely managed with `.env`.
* 🧐 **Scalable Backend Design** – Express.js server modularized for future growth (transactions, reporting, etc).

---

## 🧱 Tech Stack

| Layer      | Technology                           |
| ---------- | ------------------------------------ |
| Frontend   | React.js, Tailwind                   |
| Backend    | Node.js, Express                     |
| Database   | MSSQL (SQL Server)                   |
| Auth Layer | Username + Password (bcrypt planned) |
| Security   | Environment Variables                |

---

## 📁 Project Structure

```
finance-tracker/
├── client/         # React Frontend
│   └── src/
│       └── components/
├── server/         # Node.js + Express Backend
│   ├── index.js
│   └── .env
└── README.md
```

---

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/finance-tracker.git
cd finance-tracker
```

### 2. Setup MSSQL Database

Run the following SQL commands in **SSMS**:

```sql
CREATE DATABASE financeApp;

USE financeApp;

CREATE TABLE Users (
  id INT PRIMARY KEY IDENTITY(1,1),
  username NVARCHAR(50) UNIQUE NOT NULL,
  password NVARCHAR(255) NOT NULL
);

INSERT INTO Users (username, password)
VALUES ('testuser', '123456');
```

### 3. Configure Environment

Create a `.env` file inside `/server/`:

```
DB_USER=your_db_user
DB_PASS=your_db_password
DB_SERVER=localhost\SQLEXPRESS
DB_NAME=financeApp
```

---

### 4. Run the Backend

```bash
cd server
npm install
node index.js
```

### 5. Run the Frontend

```bash
cd client
npm install
npm start
```

---

## 🧠 Project Purpose (Resume-Grade Summary)

> Developed a **secure, full-stack finance tracking platform** using React, Node.js, and MSSQL. Engineered a custom login system leveraging Express and SQL parameterized queries. Architected the database schema, integrated environment-based secrets, and structured the codebase for future expansion (e.g., expense analytics, investment planning). Designed for scalability and production deployment.

---

## 📌 Future Enhancements

* 🔒 Hashing & salting passwords with `bcrypt`
* 📊 Dashboard charts using `Recharts` or `Chart.js`
* 🗕️ Monthly expense categorization
* 🌐 Deployment on Vercel + Azure SQL or Railway

---

## 👨‍💼 Author

**\[Your Name]**
`Full-stack Developer | React | Node | MSSQL`

---

## 📃 License

This project is licensed under the MIT License.
