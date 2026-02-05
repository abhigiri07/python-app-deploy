## 🚀 Python Flask Web App with Gunicorn (AWS EC2)

This project is a simple yet production-style **Python Flask web application** deployed on an **AWS EC2 instance** and served using **Gunicorn**.  
The app allows users to submit data via a web UI and stores it in a database.

This project demonstrates real-world backend deployment concepts like:
- Virtual environments
- Gunicorn WSGI server
- EC2 networking

---

### 🛠 Tech Stack

- **Python 3.12**
- **pip**
- **Flask**
- **Gunicorn**
- **SQLite**
- **AWS EC2 (Ubuntu)**
- **HTML & CSS**

---

## 📁 Project Structure

my_pythonapp/ 
<br>
├── app.py   <br>
├── requirements.txt  <br>
├── users.db   <br>
├── myenv/   <br>
└── templates/  <br>
├── index.html  <br>
└── users.html

---

## ⚙️ Application Features

- User-friendly web interface
- Insert user data (name & email)
- Store data in SQLite database
- View inserted records
- Production-ready Gunicorn server

---

### EC2 Security Group Configuration

Ensure the EC2 security group allows inbound traffic:

```TCP	    5000    0.0.0.0/0```

---

### 🐍 Python & pip Installation (Ubuntu / EC2)

Update system packages:
```bash
sudo apt update
```

Install Python3 and pip:
```bash
sudo apt install python3 python3-pip python3-venv -y
```

Verify installation:
```bash
python3 --version
pip3 --version
```

---
## 🚀 Setup & Installation

### 1️⃣ Clone or copy the project
```bash
cd ~
mkdir my_pythonapp
cd my_pythonapp
```
 ### 2️⃣ Create Python virtual environment
 ```bash
python3 -m venv myenv
source myenv/bin/activate
```

### 3️⃣ Install dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### ▶️ Running the Application
🔹 Run with Flask (Development)
```
python3 app.py
```
![](./images/Screenshot%20(259).png)


🔹 Run with Gunicorn (Production-style)
```
gunicorn --bind 0.0.0.0:5000 app:app --daemon
```
![](./images/Screenshot%20(263).png)

Access:
```
http://<EC2-PUBLIC-IP>:5000
```
![](./images/Screenshot%20(260).png)
![](./images/Screenshot%20(261).png)
