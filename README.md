# NLC Integrated Gate Pass System (IGPS)

![Live Status](https://img.shields.io/badge/Status-Live-success)
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Flask](https://img.shields.io/badge/Flask-Backend-black)
![MySQL](https://img.shields.io/badge/MySQL-Database-orange)
![License](https://img.shields.io/badge/License-MIT-green)

A Full-Stack, Role-Based Access Control (RBAC) web application designed to digitize and streamline the process of issuing, approving, and verifying gate passes for employees, visitors, and materials at NLC India Limited. 

This project completely transitions the traditional paper-based gate pass workflow into a secure, fast, and fully audited digital ecosystem.

## 🚀 Live Demo

You can test the fully functional live application here:
**[Live Website - Railway Deployment](https://nlc-integrated-gatepass-system.onrender.com)**

> **Note:** The application is hosted using Railway''s services. If the instance has spun down due to inactivity, the initial load may take a few moments.

### Demo Credentials
To explore the different role-based dashboards, you can log in using any of the following test accounts:

| Role | Email | Password |
| :--- | :--- | :--- |
| **Admin** | \dmin@nlcindia.com\ | \password123\ |
| **Manager** | \manager@nlcindia.com\ | \password123\ |
| **Security** | \security@nlcindia.com\ | \password123\ |
| **Employee** | \employee@nlcindia.com\ | \password123\ |

---

## ✨ Key Features

- **Role-Based Dashboards**: Distinct, secure portals tailored for Employees, Managers, Security Personnel, and System Admins.
- **Strict Authorization Boundaries**: API endpoints are locked down based on JWT claims and database-level \is_active\ user status checks. 
- **Unified Timeline Generation**: Merges diverse database models (Gate Passes, Visitor Passes, Material Passes) into a single, chronologically sorted API stream.
- **Secure Authentication**: Built entirely with JWT (JSON Web Tokens) and Werkzeug password hashing.
- **Non-Destructive Data Retention**: Implements soft-deletion (\is_active\ toggling) to maintain historical database integrity for security audits.
- **Dynamic Frontend**: A Single Page Application (SPA) feel built with Vanilla JavaScript and dynamic DOM manipulation.

## 🛠️ Technology Stack

* **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6)
* **Backend**: Python, Flask, Flask-JWT-Extended, PyMySQL
* **Database Engine**: MySQL 
* **ORM**: SQLAlchemy
* **Deployment Infrastructure**: Railway (Managed MySQL Database & Python Web Service)

## 💻 Running Locally

If you want to run this project on your own machine:

1. **Clone the repository**
   \\ash
   git clone https://github.com/mohamedhanifa27/NLC-GATEPASS-SYSTEM.git
   cd NLC-GATEPASS-SYSTEM
   \
2. **Install Dependencies**
   \\ash
   pip install -r requirements.txt
   \
3. **Set up Environment Variables**
   Create a \.env\ file in the root directory and provide your database credentials:
   \\env
   DATABASE_URL=mysql+pymysql://username:password@localhost/igps_db
   JWT_SECRET_KEY=your_secure_random_string
   \
4. **Initialize the Database**
   \\ash
   python init_db.py
   \
5. **Run the Server**
   \\ash
   python app.py
   \   Navigate to \http://localhost:5000\ in your browser.

## 🤝 Contribution & License

Created and maintained by [Mohamed Hanifa](https://github.com/mohamedhanifa27). 

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
