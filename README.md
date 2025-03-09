# Trading Card Inventory Tracking App

## Overview

We need a web-based tracking app to manage trading card inventory, purchases, sales, grading, and transactions. This app should process data from **Cards 2020.xlsx** and provide an interactive way to view, search, and track card-related information.

The goal is to create a **GitHub Pages site** that dynamically loads data from the Excel sheet (or a converted JSON file) to allow efficient inventory tracking without requiring manual spreadsheet access.

---

## Key Features

### 1. Inventory Management (from `All Purchases` & `Sealed`)
- Display a list of **all purchased** cards with details such as:
  - Item Name
  - Era (Gen 3, WOTC, etc.)
  - Type (Raw Single, ETB, etc.)
  - Condition (LP, NM, etc.)
  - Purchase Price
  - Arrival Date
  - Status (Arrived, Pending, etc.)
- Show **sealed product inventory** separately with set name, type, quantity, and storage location.
- Implement **search and filtering** by name, condition, or set.

### 2. Sales Tracking (from `Selling`)
- Show items that are listed or sold.
- Display details such as:
  - Sale Price
  - Original Purchase Price
  - Profit Calculation
- Provide a simple **profit/loss analysis** for each item.

### 3. Grading Log (from `Grading`)
- Display **graded cards** with:
  - Card Name
  - Calculated Grade
  - PSA Grade (if available)
  - Individual grading scores (Surface, Edges, Corners, Centering)
  - Any **blemishes** noted in the spreadsheet.

### 4. Transaction History (from `txn hist` & `purchases Jul22`)
- Track **where purchases were made**, including:
  - Seller Name
  - Purchase Date
  - Transaction Amount
  - Payment Method (PayPal, Apple Pay, etc.)
  - Associated items for each transaction.
- Display **total spending analysis** over time.

---

## Technical Approach

### **Frontend (GitHub Pages Site)**
- **React-based UI** (or Vanilla JavaScript with DataTables for simplicity).
- **CSV/Excel parsing** using **SheetJS (xlsx library)** to process `Cards 2020.xlsx` dynamically.
- **Bootstrap or TailwindCSS** for styling and a clean interface.

### **Data Handling**
- Convert `Cards 2020.xlsx` to **JSON format** on initial load.
- Store processed data in a **local JSON file** (for static access) or integrate with **Google Sheets** for live updates.

### **Hosting**
- **GitHub Pages** (for a simple static frontend).
- Consider **Firebase or Supabase** if write access (updates) is needed.
