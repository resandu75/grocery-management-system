# FreshMart Grocery Management System

A grocery-store management project adapted from the supplied Pharmacy Management System project. It uses **React + Vite**, **Spring Boot (Java 17)** and **MySQL 8**.

## Features
- Staff login and role-based access (Manager, Storekeeper, Inventory, Finance, Cashier)
- Product catalog (name, brand, category, barcode, price, reorder levels)
- Inventory batches, expiry dates, stock alerts and branch transfers
- Suppliers, purchasing and supplier payments
- POS sales, invoices, customers and loyalty points
- Special orders (adapted from the original prescription workflow)
- Dashboard, reporting, financial and staff tools

## Set up database
1. Install MySQL 8, Java 17+, Node.js 18+ and Maven.
2. In MySQL Workbench, open and execute `database/schema.sql`. **Warning: script drops and recreates `grocery_management`. Do not run against a database with important data.**

## Start backend
Open a terminal in `backend`. Set environment variable `DB_PASSWORD` to your own MySQL password, then run:

Windows (PowerShell):
```powershell
$env:DB_USER="root"
$env:DB_PASSWORD="YOUR_MYSQL_PASSWORD"
./mvnw.cmd spring-boot:run
```
Linux / macOS:
```bash
export DB_USER=root
export DB_PASSWORD=YOUR_MYSQL_PASSWORD
./mvnw spring-boot:run
```
Backend API: `http://localhost:5000/api`

## Start frontend
Open a second terminal in `frontend` and run:
```bash
npm install
npm run dev
```
Open `http://localhost:5173`.

## Demo login
- Email: `manager@grocery.lk`
- Password: `password`

Other staff: `storekeeper@grocery.lk`, `inventory@grocery.lk`, `finance@grocery.lk`, `cashier@grocery.lk` (same initial password). Change demo passwords before any real deployment.

## Notes
- This is a **development/academic project**, not a security-audited production system.
- Imported implementation retains some advanced workflows from the supplied reference, renamed to grocery terminology.
- The full project requires MySQL; opening `index.html` directly will not run it.
- Source files only are included; dependencies must be installed on the machine.
