# Pharmacy Management System

> A comprehensive internal management system for local pharmacies and medical stores — medicine inventory, sales, billing, customer records, and admin controls, all in one.

---

## Overview

Small and mid-size pharmacies typically manage inventory in spreadsheets and billing on paper. This system replaces that with a structured, web-based management platform designed specifically for the workflow of a local pharmacy.

Built for real-world deployment: a working system, not a demo.

---

## Features

### Inventory Management
- Add, update, and remove medicines with batch number, expiry date, and quantity
- Low-stock alerts when medicine quantity falls below a configurable threshold
- Expiry tracking with upcoming-expiry warnings

### Sales & Billing
- Point-of-sale interface: search medicines, add to cart, apply discounts
- Auto-generated itemised bills with GST breakdown
- Print-ready invoice generation

### Customer Records
- Customer profiles with purchase history
- Search by name or phone number
- Outstanding balance tracking

### Payments
- Record payments against bills
- Mark invoices as paid / partially paid / unpaid
- Payment history log per customer

### Reports & Analytics
- Daily, weekly, and monthly sales summaries
- Top-selling medicines
- Revenue and profit charts

### Admin & Security
- Role-based access: Admin and Staff roles
- Secure login with password hashing
- Session management

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | PHP |
| Database | MySQL |
| Frontend | HTML · CSS · JavaScript |
| Auth | PHP Sessions + bcrypt password hashing |
| Charts | Chart.js |

---

## Getting Started

### Prerequisites

- PHP 7.4+
- MySQL 5.7+
- A local server (XAMPP, WAMP, or LAMP)

### Installation

```bash
# Clone the repository
git clone https://github.com/rahul4018/pharmacy-management-system-porject.git
cd pharmacy-management-system-porject
```

1. Start Apache and MySQL via XAMPP (or your local server)
2. Open `http://localhost/phpmyadmin`
3. Create a new database named `pharmacy_db`
4. Import `database/pharmacy_db.sql`
5. Update `config/db.php` with your database credentials:

```php
<?php
$host = 'localhost';
$dbname = 'pharmacy_db';
$username = 'root';
$password = '';
```

6. Open `http://localhost/pharmacy-management-system-porject` in your browser

### Default Admin Login

```
Username: admin
Password: admin123
```

> Change this immediately after first login.

---

## Project Structure

```
pharmacy-management-system/
├── config/
│   └── db.php              # Database connection
├── database/
│   └── pharmacy_db.sql     # Schema + seed data
├── modules/
│   ├── inventory/          # Medicine CRUD
│   ├── billing/            # Sales & invoices
│   ├── customers/          # Customer management
│   ├── payments/           # Payment tracking
│   └── reports/            # Analytics & charts
├── assets/
│   ├── css/
│   └── js/
├── auth/
│   ├── login.php
│   └── logout.php
└── index.php
```

---

## Screenshots

> Add screenshots here — dashboard, POS screen, inventory list, and a generated invoice make the strongest impression.

---

## Roadmap

- [ ] Barcode scanner integration for medicine lookup
- [ ] WhatsApp/SMS billing to customers
- [ ] Supplier management and purchase orders
- [ ] Mobile-responsive design
- [ ] Export reports to Excel/PDF

---

## License

MIT
