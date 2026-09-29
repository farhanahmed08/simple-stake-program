# 🎮 Simple Casino Game (Python & MySQL)
An interactive, command-line betting and logic game built with **Python** and integrated with a **MySQL** database for user account management, persistent balance tracking, and session game stats.

---

## 🌟 Features
- **User Authentication:** Create an account and securely log in to track your personal game statistics.
- **Dynamic Difficulty Levels:** Select from 4 different levels (1 to 4 bombs hidden across 25 grid choices) with increasing multipliers.
- **Persistent Progress:** Balance, tokens, total money won, and total money lost are saved directly to a MySQL database.
- **Parameterized SQL Queries:** Prevents SQL syntax errors and basic SQL injection vulnerabilities.
- **Token System:** Players start with 5 game tokens; winning a complete round awards additional tokens.

---

## 🛠️ Tech Stack
- **Language:** Python 3.13
- **Database:** MySQL
- **Connector:** `mysql-connector-python`

---

## 📋 Database Setup
Before running the application, make sure MySQL is running locally and set up the `stake` database and `stake` table:

```sql
CREATE DATABASE stake;
USE stake;

CREATE TABLE game (
    User VARCHAR(50) PRIMARY KEY,
    Pass VARCHAR(50) NOT NULL,
    Moneywon INT DEFAULT 0,
    Moneylost INT DEFAULT 0,
    Tokens INT DEFAULT 5,
    Moneyused INT DEFAULT 0
);
