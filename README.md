# Flask SQL Injection Lab

A simple Flask application designed to demonstrate SQL injection vulnerabilities. Built as a practical assignment for the **Application Security** course at SLTC.



## 🧪 Lab Overview

This lab explores:
- How SQL Injection vulnerabilities occur
- How to exploit them through login and search forms
- How to **fix** them using parameterized queries

You’ll build a vulnerable Flask app, hack it, then secure it.



## 🛠️ Tech Stack

- Python 3
- Flask
- SQLite3
- HTML (Jinja2 Templates)



## 📁 Project Structure

```

sql_injection_lab/
├── app.py               # Main Flask application
├── templates/           # HTML templates
│   ├── home.html
│   ├── login.html
│   ├── welcome.html
│   └── search.html
├── users.db             # SQLite database (auto-generated)
└── venv/                # (Optional) Python virtual environment
````



## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/AchiraNadeeshan/flask-sql-injection-lab.git
cd flask-sql-injection-lab
````

### 2. Setup Environment

```bash
python -m venv venv
# Activate (Linux/Mac)
source venv/bin/activate
# Activate (Windows)
venv\Scripts\activate
```

### 3. Install Flask

```bash
pip install flask
```



## 🔍 Lab Tasks Summary

* ✅ Create Flask app with intentional SQL injection vulnerabilities
* ✅ Implement `/login` and `/search` routes using unsafe queries
* ✅ Test exploits using:

  * `admin' OR '1'='1`
  * `' OR '1'='1`
* ✅ Fix vulnerabilities using parameterized queries



## 🔐 After Fixes

* Uses `?` placeholders to prevent injections:

  ```python
  cursor.execute("SELECT * FROM users WHERE username = ? AND password = ?", (username, password))
  ```



## ✅ Commit Style

This repo uses **Conventional Commits**, e.g.:

```
feat: implement vulnerable login form
fix: patch SQL injection in login route
chore: add .gitignore and Flask setup
```


## 📄 License

This lab is for educational use only as part of the Application Security module.
