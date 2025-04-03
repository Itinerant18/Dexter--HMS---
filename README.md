# 🚀 **Dexter Web Application (Version 2.0.2 - README**

---

## 🌟 1. Introduction & Purpose

Welcome to **Dexter Web Application** – a powerful, user-friendly control panel designed for **device management, system monitoring, and network control**. This **Flask-based web application** provides a seamless and intuitive experience, enabling users to configure and monitor their devices effortlessly.

### 🔥 **Key Benefits**
✅ **Modern Web Interface** – Sleek, responsive, and mobile-friendly UI.  
✅ **Full System Control** – Manage device settings, network configurations, and power zones.  
✅ **Secure Authentication** – User login with session handling.  
✅ **Data Persistence** – Stores settings in SQLite databases & config files.  
✅ **Easy File Uploads** – Upload and manage files directly through the web interface.  

---

## 🎯 2. Features & Functionality

### 🎨 **User Interface (UI)**
✨ **Fully Responsive:** Works across desktops, tablets, and mobile devices.  
✨ **Interactive Elements:** Dropdowns, toggles, and buttons for seamless control.  
✨ **Dark & Light Theme Ready:** (Future-proof for UI enhancements).  

### ⚡ **System Management**
✔ **Advanced Settings:** Modify system parameters via an intuitive UI.  
✔ **Sleep Mode & Reset:** Put the system in sleep mode or restore default settings.  
✔ **Zone Management:** Configure zones using `zone.txt` and `powerZoneSettings.txt`.  
✔ **Network Configuration:** Manage network settings via `modem_config.db`.  
✔ **Authentication:** Secure login system for admin users.  

### 🔄 **Data Storage & Persistence**
🗂 **SQLite Databases:**  
   - `sepleDB.db` → Core system data.  
   - `dexterpanel2.db` → Control panel settings.  
   - `modem_config.db` → Network configurations.  
📁 **Config Files:** Stores user settings (`zone.txt`, `powerZoneSettings.txt`).  
📤 **Uploads Folder:** Secure file upload system.  

---

## 🏗 3. Architecture & Workflow

**📌 Architecture Overview:**
1️⃣ **Client (Browser)** → Loads UI & interacts with the server.  
2️⃣ **Flask Web Server** → Handles requests, processes system actions.  
3️⃣ **Database & Config Files** → Stores and retrieves system settings.  
4️⃣ **Managed Devices** → Interfaces with connected hardware.  

🔄 **Typical User Flow:**
1️⃣ **Login** 🔑 → 2️⃣ **Navigate Settings** ⚙ → 3️⃣ **Modify & Save** ✅ → 4️⃣ **System Updates** 🔄

---

## 🛠 4. Technology Stack

📌 **Backend:** Python 3.x (Flask)  
📌 **Frontend:** HTML5, CSS3, JavaScript  
📌 **Templating Engine:** Jinja2  
📌 **Database:** SQLite  
📌 **Python Libraries:** Flask, Flask-SQLAlchemy, Flask-Login, Requests, Pyserial  

---

## 📂 5. Project Structure

```
📦 Dexter Web App
├── 📜 seple.py           # Main Flask app
├── 📜 requirements.txt   # Dependencies
├── 📂 templates/         # UI Templates (HTML)
│   ├── layout.html       # Base template
│   ├── advanced.html     # Advanced settings page
├── 📂 static/            # Frontend assets
│   ├── css/             # Stylesheets
│   ├── js/              # JavaScript files
├── 📂 uploads/           # File uploads
├── 📂 databases/         # Data storage
│   ├── sepleDB.db        # Core system database
│   ├── dexterpanel2.db   # Panel settings
│   ├── modem_config.db   # Network configurations
├── 📂 config/            # Configuration files
│   ├── zone.txt
│   ├── powerZoneSettings.txt
│   ├── powerzone.txt
```

---

## 🚀 6. Installation & Running

### 🛑 **Prerequisites**
🔹 Python 3.x  
🔹 pip  
🔹 Git (for cloning repository)  

### 📌 **Setup Instructions**

1️⃣ **Clone the Repository**  
```bash
$ git clone <your-repository-url>
$ cd Dexterweb2.0.2
```

2️⃣ **Create & Activate Virtual Environment**  
```bash
$ python -m venv .venv
$ source .venv/bin/activate   # macOS/Linux
$ .\.venv\Scripts\activate   # Windows
```

3️⃣ **Install Dependencies**  
```bash
$ pip install -r requirements.txt
```

4️⃣ **Run the Application**  
```bash
$ python seple.py
```

5️⃣ **Access Dexter in Browser**  
🔗 Open: `http://127.0.0.1:5000/`

---

## 🔒 7. Security Considerations

🚧 **Input Validation:** Prevent XSS & SQL Injection.  
🔐 **Authentication:** Secure user login & session handling.  
🛑 **Disable Debug Mode:** Avoid `debug=True` in production.  
📁 **File Upload Security:** Restrict file types & sizes.  

---

## 🔧 8. Troubleshooting

❌ **ModuleNotFoundError:** Activate the virtual environment before running.  
❌ **Database Errors:** Ensure `.db` files exist with correct permissions.  
❌ **Static Files Not Loading:** Verify correct paths (`url_for('static', filename='...')`).  

---

## 🤝 9. Contributing

💡 Found an issue? Open a **GitHub Issue**!  
📌 Want to contribute? Submit a **Pull Request** with a detailed description!  

---

## 📜 10. License

📖 This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

## 📧 11. Contact / Support

📩 For questions or support, contact: **[itinerant018@gmail.com]**  

---

🎉 **Thank you for using Dexter Web Application!** 🚀
