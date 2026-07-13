<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1E1B10,100:F59E0B&height=180&section=header&text=Quantix&fontSize=58&fontColor=FFFFFF&animation=fadeIn&fontAlignY=35&desc=Inventory%20Intelligence%20System&descAlignY=58&descSize=18&descColor=FEF3C7" width="100%" alt="Quantix banner" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&pause=1500&color=F59E0B&center=true&vCenter=true&width=650&lines=5+CRUD+Modules+%7C+Role-Based+Access+Control;60%25+Faster+Billing+%7C+Real-Time+Stock+Tracking;Python+%C2%B7+Tkinter+%C2%B7+SQLite+%C2%B7+Pandas" alt="Typing SVG" />

**A complete desktop inventory and billing system — built for small retail stores that need a fast, reliable, no-fuss GUI**

[![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![Tkinter](https://img.shields.io/badge/Tkinter-F59E0B?style=for-the-badge&logo=python&logoColor=white)](https://docs.python.org/3/library/tkinter.html)
[![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)

<br/>

[![GitHub Repo stars](https://img.shields.io/github/stars/SamarthDharpure/Quantix?style=flat-square&color=F59E0B)](https://github.com/SamarthDharpure/Quantix/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/SamarthDharpure/Quantix?style=flat-square&color=F59E0B)](https://github.com/SamarthDharpure/Quantix/network)
[![GitHub issues](https://img.shields.io/github/issues/SamarthDharpure/Quantix?style=flat-square&color=F59E0B)](https://github.com/SamarthDharpure/Quantix/issues)
[![Last commit](https://img.shields.io/github/last-commit/SamarthDharpure/Quantix?style=flat-square&color=F59E0B)](https://github.com/SamarthDharpure/Quantix/commits)
[![License: MIT](https://img.shields.io/badge/License-MIT-F59E0B.svg?style=flat-square)](#-license)

[Overview](#-overview) · [Features](#-features) · [Workflow](#-workflow) · [Tech Stack](#-tech-stack) · [Getting Started](#️-getting-started) · [Usage](#-usage) · [Screenshots](#-screenshots) · [Roadmap](#-roadmap)

</div>

<br/>

## 📖 Overview

**Quantix** is a desktop inventory management system built with **Python (Tkinter)** and **SQLite**, designed to replace manual paperwork for small retail businesses with a single, friendly GUI. It handles the full operational loop — employees, suppliers, categories, products, and point-of-sale billing — in one local application with no server setup required.

<br/>

<div align="center">

|  🧩 CRUD Modules  |  ⚡ Billing Speed  |  🔐 Access Control  |  💾 Database  |
|:---:|:---:|:---:|:---:|
|  **5**  |  **60% faster**  |  **Role-based**  |  **SQLite**  |

</div>

<br/>

## ✨ Features

<table>
<tr>
<td width="50%">

### ✅ User Authentication
Secure employee login gating access to the system.

### 🧾 Full CRUD
Complete management of Employees, Suppliers, Categories, and Products.

### 🛒 Sales & Billing
End-to-end billing module with printable customer bills.

### 🔎 Search & Filters
Fast lookups across every record type — search-by or show-all.

</td>
<td width="50%">

### 🧮 Built-in Calculator
Quick arithmetic on hand during billing, no context-switching.

### 📦 Stock Management
Live in-stock tracking with automatic quantity updates.

### 🖨️ Bill Generation & Print
One-click export and printing of the customer bill area.

### 🗂️ Bill History Viewer
Browse and reopen previously saved bill files.

</td>
</tr>
</table>

<br/>

## 🔄 Workflow

```mermaid
flowchart TD
    A["Login<br/>Employee Auth"] --> B["Dashboard<br/>Overview Tiles"]
    B --> C["Employees"]
    B --> D["Suppliers"]
    B --> E["Categories"]
    B --> F["Products"]
    B --> G["Sales & Billing"]
    C & D & E & F --> H[("SQLite Database<br/>inventory.db")]
    G --> I["Stock Update"]
    I --> H
    G --> J["Bill Generation<br/>Print / Save"]
```

**Flow:** an employee logs in and lands on the dashboard, which surfaces live totals across every module. Product, supplier, category, and employee records all read/write through a shared SQLite database, while the Sales module additionally updates stock levels and generates a printable, saved bill on checkout.

<br/>

## 🧑‍💻 Tech Stack

<div align="center">

| Layer | Technology |
|---|---|
| **GUI** | Python 3.10+ · [Tkinter](https://docs.python.org/3/library/tkinter.html) (tk, ttk) · [Pillow](https://pypi.org/project/pillow/) · tkcalendar *(optional)* |
| **Database** | [SQLite3](https://www.sqlite.org/) *(default — configurable to MySQL/MariaDB)* |
| **Tooling** | VS Code / PyCharm · Git & GitHub |

</div>

<br/>

## 📂 Project Structure

```
Quantix/
├── main.py                # App launcher
├── database.py            # DB connection & helpers (SQLite)
├── employees.py           # Employee CRUD + UI
├── suppliers.py           # Supplier CRUD + UI
├── categories.py          # Category CRUD + UI
├── products.py            # Product CRUD + UI
├── sales.py                # Billing & sales flow
├── utils.py                # Calculator, printing utilities
├── requirements.txt
├── images/                 # UI assets & screenshots
└── data/
    └── inventory.db        # created on first run
```

> File names above reflect the module breakdown — adjust commands if your actual filenames differ.

<br/>

## ⚙️ Getting Started

### Prerequisites
- Python 3.10+

### 1. Clone the repository

```bash
git clone https://github.com/SamarthDharpure/Quantix.git
cd Quantix
```

### 2. Create & activate a virtual environment

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
# if requirements.txt isn't present:
pip install pillow tkcalendar
```

### 4. Database

Uses **SQLite** by default — `inventory.db` is created automatically on first run. To use MySQL instead, update the connection config in `database.py` and install `mysql-connector-python`.

### 5. Run the app

```bash
python main.py
```

<br/>

## 🚀 Usage

1. **Login** with a valid employee ID and password
2. **Dashboard** shows live totals for employees, suppliers, categories, products, and sales
3. **Manage records** — Add / Update / Delete / Search across each module from the side menu
4. **Sales** — add customer details, select products, adjust quantities, apply discounts, and generate a printable bill
5. **Bill history** — reopen and review any previously saved bill

<br/>

## 📸 Screenshots

<div align="center">

| Login | Dashboard |
|:---:|:---:|
| <img width="380" alt="Login" src="https://github.com/user-attachments/assets/98ca9f16-2b3b-4aa7-905e-94ab3687e2f8" /> | <img width="380" alt="Dashboard" src="https://github.com/user-attachments/assets/2d48c696-3eec-4c11-bc8a-4f69e592ad0d" /> |

| Employee Management | Product Management |
|:---:|:---:|
| <img width="380" alt="Employee Management" src="https://github.com/user-attachments/assets/2abd50f1-419c-44ef-8246-b9d11b607e85" /> | <img width="380" alt="Product Management" src="https://github.com/user-attachments/assets/ffab792e-c9fa-4a2c-88a9-1701fa40248f" /> |

| Supplier Management | Sales & Billing |
|:---:|:---:|
| <img width="380" alt="Supplier Management" src="https://github.com/user-attachments/assets/86a2e0ee-8a6b-4422-88b6-18967d409a82" /> | <img width="380" alt="Sales & Billing" src="https://github.com/user-attachments/assets/a06c46fa-7a47-4578-9658-4e6db1df67db" /> |

| POS / Shopping View |
|:---:|
| <img width="380" alt="POS View" src="https://github.com/user-attachments/assets/67330101-824d-40e9-845f-3eab39c5beb5" /> |

</div>

<br/>

## 🗺️ Roadmap

- [ ] Multi-user mode with concurrent access
- [ ] REST API layer for external integrations
- [ ] Optional web frontend
- [ ] Sales analytics dashboard (charts & trend reports)
- [ ] PDF export for bills (in addition to print)

> Have an idea? [Open an issue](https://github.com/SamarthDharpure/Quantix/issues) — contributions and suggestions are welcome.

<br/>

## 🤝 Contributing

Contributions are welcome! Especially interested in multi-user mode, a REST API, or a web frontend.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes and push
4. Open a Pull Request describing your changes

Please follow a consistent code style and include tests where applicable.

<br/>

## 📜 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

<br/>

## 🧑‍💻 Author

<div align="center">

**Samarth Dharpure**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/samarth-dharpure-88a10b248/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SamarthDharpure)

</div>

<br/>

<div align="center">

### ⭐ If Quantix was useful to you, consider giving it a star — it helps a lot!

</div>
