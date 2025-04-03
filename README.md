# Dexter Web Application (Version 2.0.2-copy) - README

## 1. Introduction & Purpose

Welcome to the Dexter Web Application! This is a **Python-based web application** built using the **Flask framework**. It serves as a control panel and management interface for an underlying system or set of devices.

### **Core Purpose**

Dexter functions as:
- **A Home Management System (HMS):** Controlling smart home devices, monitoring sensors, managing power usage, etc.
- **A Device Control Panel:** Providing a web interface for configuring and managing specific hardware (like network equipment, industrial controllers, or custom electronics).
- **A System Monitoring Dashboard:** Displaying system status and allowing configuration changes for a software system or service.

The application provides a user-friendly web interface, making complex configurations and system states accessible via a standard web browser, including mobile devices.

---

## 2. Key Features & Functionality

### **Web-Based User Interface**
- Accessible from desktops and mobile devices.
- Built with HTML (Jinja2 templates), CSS (styling), and JavaScript (client-side interactivity).

### **System Control & Configuration**
- **Advanced Settings (`advanced.html`):** A dedicated section for modifying system parameters.
- **Sleep Mode:** Places the managed system/device into a low-power or inactive state.
- **Reset to Default:** Reverts system settings to a predefined factory or baseline state.
- **Zone Management:** Uses `zone.txt` and `powerZoneSettings.txt` to manage operational zones and power settings.
- **Network/Modem Configuration:** Manages network settings via `modem_config.db`.
- **User Authentication:** Login and session management for secure access.

### **Data Persistence**
- Uses **SQLite databases** for data storage:
  - `sepleDB.db`: Primary database for core application data, user accounts, logs, or system state.
  - `dexterpanel2.db`: Stores the control panel’s state and interface preferences.
  - `modem_config.db`: Stores modem/network-related configurations.
- External **configuration files (`.txt`)** for flexible settings:
  - `zone.txt`, `powerZoneSettings.txt`, `powerzone.txt`: Manage zone configurations.

### **File Upload Capability**
- Users can upload files via the web interface, stored in `uploads/`.

---

## 3. Architecture & Workflow

Dexter follows a **Client-Server web application architecture**:

1. **Client (User's Browser)**
   - Renders HTML, CSS, and executes JavaScript.
   - Sends HTTP requests to the Flask server for interactions.

2. **Web Server (Flask Application - `seple.py`)**
   - Routes requests and processes system commands.
   - Handles business logic and database interactions.
   - Generates HTML templates dynamically.
   - Reads configuration settings from `.txt` files.

3. **Data Storage**
   - **SQLite Databases:** Store structured persistent data.
   - **Configuration Files:** Store specific operational parameters.
   - **Uploaded Files:** Store user-provided data.

4. **(External) Managed System/Devices** *(Highly Inferred)*
   - `seple.py` may communicate with devices via serial port, network protocols (HTTP/MQTT), or system commands.

### **Typical User Workflow**
1. User logs into the web interface.
2. Navigates to "Advanced Settings".
3. Adjusts settings and applies changes.
4. Flask processes the request and updates configurations.
5. System/device state is modified accordingly.

---

## 4. Technology Stack

- **Backend:** Python 3.x with Flask
- **Templating Engine:** Jinja2
- **Database:** SQLite 3
- **Frontend:** HTML5, CSS3, JavaScript (ES5/ES6)
- **Python Libraries Used:**
  - `Flask` (Web framework)
  - `Flask-SQLAlchemy` (ORM for database interaction)
  - `Flask-Login` / `Flask-Session` (Authentication & session management)
  - `requests` (For making HTTP requests)
  - `pyserial` (If controlling hardware via serial ports)

---

## 5. Project Structure

```
├── seple.py           # Main Flask application
├── requirements.txt   # Dependencies list
├── templates/         # HTML templates (Jinja2)
│   ├── layout.html    # Base template
│   ├── advanced.html  # Advanced Settings page
├── static/            # Frontend assets
│   ├── css/          # Stylesheets
│   ├── js/           # JavaScript files
├── uploads/          # Uploaded files
├── databases/
│   ├── sepleDB.db      # Primary database
│   ├── dexterpanel2.db # Panel-specific data
│   ├── modem_config.db # Modem settings
├── config/
│   ├── zone.txt
│   ├── powerZoneSettings.txt
│   ├── powerzone.txt
```

---

## 6. Installation & Running

### **Prerequisites**
- **Python 3.x** (Check: `python --version`)
- **pip** (Check: `pip --version`)
- **Git** (For repository cloning)

### **Setup Instructions**

1. **Clone the Repository**
   ```bash
   git clone <your-repository-url>
   cd Dexterweb2.0.2-copy
   ```

2. **Create & Activate Virtual Environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # macOS/Linux
   .\.venv\Scripts\activate   # Windows
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application**
   ```bash
   python seple.py
   ```

5. **Access Dexter in Browser**
   - Open `http://127.0.0.1:5000/`

---

## 7. Security Considerations

- **Input Validation:** Prevent XSS/SQL Injection by validating all user inputs.
- **Authentication:** Ensure proper password hashing and session management.
- **Database Security:** Use an ORM and avoid raw SQL queries.
- **Debug Mode:** Disable `debug=True` in production.
- **File Upload Handling:** Restrict allowed file types and enforce size limits.

---

## 8. Troubleshooting

- `ModuleNotFoundError:` Ensure virtual environment is activated before running.
- `Database Errors:` Check if `.db` files exist and have correct permissions.
- `Static Files Not Loading:` Verify correct paths in templates using `url_for('static', filename='...')`.

---

## 9. Contributing

- Report issues via GitHub Issues.
- Submit pull requests with detailed descriptions.

---

## 10. License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## 11. Contact / Support

For questions or support, contact: **[your-email@example.com]**

---

This README serves as a detailed guide for setting up, running, and understanding the Dexter Web Application.
