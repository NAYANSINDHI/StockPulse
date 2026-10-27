# 📦 StockPulse — Inventory & Sales Management System

### Smarter inventory tracking. Better stock visibility. Data-driven business decisions.

StockPulse is a web-based inventory and sales management application designed to help businesses manage products, monitor stock levels, record sales, track replenishments, and review inventory performance through a centralized dashboard.

Built with **Python, Flask, and a modular backend architecture**, StockPulse organizes common inventory workflows into a single application.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?logo=python" alt="Python" />
  <img src="https://img.shields.io/badge/Flask-Web%20Framework-black?logo=flask" alt="Flask" />
  <img src="https://img.shields.io/badge/Database-SQLite%20%7C%20PostgreSQL-blue" alt="Database" />
  <img src="https://img.shields.io/badge/Architecture-Modular-success" alt="Architecture" />
</p>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [Application Architecture](#-application-architecture)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [API Overview](#-api-overview)
- [Configuration](#-configuration)
- [Screenshots](#-screenshots)
- [Future Enhancements](#-future-enhancements)
- [Learning Outcomes](#-learning-outcomes)
- [Author](#-author)

## 🚀 Overview

Managing inventory manually can make it difficult to track product quantities, record sales accurately, monitor incoming stock, and understand business performance.

StockPulse aims to simplify these activities by providing a centralized web application for inventory and sales operations.

The application separates functionality into dedicated Flask route modules, making the backend easier to maintain and extend. Its dashboard brings together inventory information, transaction summaries, and key business metrics.

### 🎯 Project Objectives

- Centralize product and inventory information.
- Maintain accurate stock quantities as sales are recorded.
- Track incoming stock and replenishment activities.
- Organize sales transactions and inventory movements.
- Present useful business metrics through a dashboard.
- Support inventory reporting and operational analysis.

## ✨ Key Features

### 🔐 Authentication and User Management
- Login and authentication functionality.
- Session or token management utilities.
- Authentication helpers for protected application workflows.

### 📊 Dashboard and Analytics
- Overview of inventory levels and business metrics.
- Recent transaction information.
- Sales summaries and inventory-related statistics.

### 📦 Product Management
- Maintain a product catalog.
- Organize product categories, pricing, and quantities.
- Support product creation, viewing, updating, and deletion.

### 📉 Inventory Tracking
- Record inventory adjustments.
- Monitor available stock quantities.
- Keep stock information aligned with supported sales and replenishment workflows.

### 🚚 Restock Management
- Record incoming stock and replenishment batches.
- Track stock additions.
- Update inventory quantities through supported restocking operations.

### 💳 Sales Management
- Record sales transactions.
- Maintain sales history.
- Deduct sold quantities from inventory through the sales workflow.

### 📑 Reports and Business Insights
- Review inventory movements.
- Analyze recorded sales and revenue information.
- Generate operational reports through the reporting module.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python 3.10+ | Backend programming |
| Flask | Web application framework |
| Flask Blueprints / route modules | Organizing backend functionality |
| SQLite / PostgreSQL | Database options, depending on configuration |
| HTML | Web interface |
| CSS and JavaScript | Frontend styling and interactions, where implemented |
| REST-style API routes | Communication between frontend and backend |

**Note:** The repository contains multiple implementations. The setup instructions below target the `stockpulse_app_v2` Flask application. The exact dependencies and database configuration should be confirmed in that implementation's `requirements.txt`, `config.py`, and `db.py`.

## 🏗️ Application Architecture

The main Flask implementation follows a modular architecture.

```text
                  ┌─────────────────────┐
                  │     Web Browser     │
                  │    User Interface   │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │    Flask Backend    │
                  │      app.py         │
                  └──────────┬──────────┘
                             │
           ┌─────────────────┼──────────────────┐
           │                 │                  │
           ▼                 ▼                  ▼
    ┌────────────┐    ┌────────────┐     ┌────────────┐
    │  Products  │    │ Inventory  │     │   Sales    │
    └────────────┘    └────────────┘     └────────────┘
           │                 │                  │
           └─────────────────┼──────────────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │ Database Layer      │
                  │ db.py / config.py   │
                  └─────────────────────┘
```

The application also includes separate modules for authentication, dashboard metrics, restocking, and reporting.

## 📂 Project Structure

The repository contains multiple implementations. The following structure describes the primary `stockpulse_app_v2` implementation.

```text
StockPulse/
│
├── stockpulse_app_v2/
│   ├── app.py
│   ├── config.py
│   ├── db.py
│   ├── auth_helpers.py
│   ├── requirements.txt
│   │
│   ├── routes/
│   │   ├── __init__.py
│   │   ├── auth.py
│   │   ├── dashboard.py
│   │   ├── products.py
│   │   ├── inventory.py
│   │   ├── restocks.py
│   │   ├── sales.py
│   │   └── reports.py
│   │
│   └── static/
│       └── index.html
│
├── stockpulse_hybrid/
├── stockpulse_php/
└── Readme.md
```

### Backend Module Responsibilities

| Module | Responsibility |
|---|---|
| `app.py` | Initializes and runs the Flask application |
| `config.py` | Application and database configuration |
| `db.py` | Database connections and query helpers |
| `auth_helpers.py` | Authentication and session-related utilities |
| `routes/auth.py` | Authentication endpoints |
| `routes/dashboard.py` | Dashboard metrics and summaries |
| `routes/products.py` | Product catalog operations |
| `routes/inventory.py` | Stock-level management |
| `routes/restocks.py` | Incoming stock and replenishment |
| `routes/sales.py` | Sales transaction operations |
| `routes/reports.py` | Reporting functionality |
| `static/index.html` | Web interface entry point |

## ⚙️ Getting Started

Follow these steps to run the Flask implementation locally.

### Prerequisites

- Python 3.10 or later
- Git
- A terminal or command prompt
- A supported database configuration: SQLite or PostgreSQL

### 1. Clone the Repository

```bash
git clone https://github.com/NAYANSINDHI/StockPulse.git
cd StockPulse
```

### 2. Navigate to the Flask Application

```bash
cd stockpulse_app_v2
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

On macOS or Linux:

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 5. Configure the Application

Review `config.py` and `db.py` to determine the required database settings and application configuration.

Before running the application:

- Select and configure a supported database.
- Set any required environment variables.
- Configure a secure secret key for session management if required.
- Ensure that the database initialization or schema setup steps documented by the code are complete.

Do not commit production credentials or secret keys to GitHub.

### 6. Run the Application

```bash
python app.py
```

### 7. Open the Application

The existing README specifies the default local address as:

**http://127.0.0.1:5000**

Open this address in your browser if the application starts on the default Flask port. If `app.py` specifies another host or port, use that address instead.

## 🔌 API Overview

The Flask application organizes its API functionality into dedicated route modules.

| Route module | Functionality |
|---|---|
| `auth.py` | User authentication and session management |
| `dashboard.py` | Dashboard statistics and summaries |
| `products.py` | Product catalog operations |
| `inventory.py` | Inventory adjustments and stock queries |
| `sales.py` | Sales recording and transaction history |
| `restocks.py` | Stock replenishment records |
| `reports.py` | Inventory and sales reports |

The exact HTTP methods, endpoint URLs, request parameters, and response formats are defined in the route implementations. Refer to those files when integrating the API with another frontend.

## 📸 Screenshots

Add screenshots of the actual running application to make the repository easier for visitors to evaluate.

Recommended screenshots:

1. Dashboard overview
2. Product management page
3. Inventory and stock levels
4. Sales transactions
5. Restock management
6. Reports and analytics

Once screenshots are committed to the repository, embed them with Markdown. For example:

```markdown
![StockPulse Dashboard](screenshots/dashboard.png)
```

Replace the example filename with the actual screenshot path.

## 🔮 Future Enhancements

Possible future improvements include:

- Low-stock alerts and configurable reorder thresholds.
- Interactive inventory and sales charts.
- CSV and Excel report exports.
- Product barcode scanning.
- Supplier and purchase-order management.
- Role-based access control with clearly defined permissions.
- Audit logs for stock adjustments and sales.
- Automated tests for inventory and sales workflows.
- Cloud deployment and production database configuration.

These are proposed enhancements, not claims about currently implemented functionality.

## 🎓 Learning Outcomes

StockPulse provides practical experience with:

- Developing web applications using Python and Flask.
- Organizing backend logic into modular route handlers.
- Connecting a web application to a relational database.
- Implementing CRUD operations for business records.
- Managing inventory changes across sales and replenishment workflows.
- Creating dashboard and reporting functionality.
- Designing and documenting API endpoints.
- Using Git and GitHub for source-code management.

## 👨‍💻 Author

**Nayan Sindhi**

MCA Student | Python | SQL | Data Analytics | Web Development

- **GitHub:** [@NAYANSINDHI](https://github.com/NAYANSINDHI)
- **Repository:** [StockPulse](https://github.com/NAYANSINDHI/StockPulse)

---

## 📄 License

Review the repository's license file before redistributing or reusing this project. If no license is present, the project should not be assumed to have an open-source license.

## ⚠️ Disclaimer

StockPulse is documented here as an inventory and sales management application based on the repository's current description. It is not presented as a stock-market trading, investment recommendation, or financial analysis platform.

If this repository is intended to become a stock-market analysis application, its project overview, features, architecture, and setup instructions should be revised to match the actual financial-market implementation.
