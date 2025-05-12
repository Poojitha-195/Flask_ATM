# 🏦 ATM Web Application

A web-based ATM system developed using **Flask** and **MySQL**, which simulates basic banking functionalities such as withdrawals, deposits, PIN generation, and mini statement viewing. This project is a great demonstration of full-stack development skills using Python.

---

## 🚀 Features

- 🔐 **PIN Generation** – Securely set up a new PIN
- 💳 **User Authentication** – Login using account number and PIN
- 💰 **Withdraw Money** – With balance checks and updates
- 💸 **Deposit Money** – Adds amount to current balance
- 📄 **Mini Statement** – Displays account info and balance

---

## 🛠️ Technologies Used

- **Frontend**: HTML, Jinja Templates (via Flask)
- **Backend**: Python (Flask Framework)
- **Database**: MySQL
- **Connector**: PyMySQL

---

## 📁 Folder Structure

ATM-Web-App/
│
├── templates/
│ ├── home.html
│ ├── withdraw1.html
│ ├── withdraw2.html
│ ├── deposit1.html
│ ├── ministatement1.html
│ ├── ministatement2.html
│ ├── pingeneration1.html
│ └── pingeneration2.html
│
├── app.py
└── README.md


---

## ⚙️ How to Run the Project

1. **Create MySQL Database:**

   - Database Name: `ATM`
   - Table Name: `ACCOUNTS`

   ```sql
   CREATE TABLE ACCOUNTS (
       USER_ID INT PRIMARY KEY AUTO_INCREMENT,
       USER_NAME VARCHAR(100),
       USER_EMAIL VARCHAR(100),
       USER_ACCNO VARCHAR(20) UNIQUE,
       USER_PIN INT,
       USER_BALANCE INT
   );


Install Required Python Libraries:
pip install flask pymysql
python app.py

Open your browser and go to:
http://127.0.0.1:5000/

✅ Sample Functionalities Flow
Withdraw → Enter Account No. & PIN → Enter Amount → Balance updated if sufficient funds

Deposit → Enter Account No. & Amount → Balance updated

Mini Statement → Enter Account No. & PIN → View name, email, and balance

PIN Generation → Enter Account No. → Set and confirm new PIN

📌 Notes
All user input is handled via secure form submissions.

Basic validations are implemented.

You can customize the HTML files under /templates/ for styling and user interface improvements.

🙌 Acknowledgements
Thanks to the resources and tutorials that helped build this educational project. This system demonstrates core backend and database integration skills with Python.
