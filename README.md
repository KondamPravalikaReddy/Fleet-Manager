# Fleet Manager – Operations Portal

A single-page **Fleet Operations Dashboard** built using plain **HTML, CSS, and JavaScript**.
This portal helps track fleet equipment, work assignments, and utilization with features like CSV import/export, dark mode, and a collapsible sidebar.

---

## 🚀 Features

### 📊 Dashboard Overview

* KPI cards for:

  * Total Fleet
  * Available
  * Working
  * Maintenance
* Status distribution bar with legend
* Recent activity list based on latest equipment updates

### 🚚 Fleet Inventory

* Search by fleet number or description
* Filter by status and equipment type
* Status badges:

  * Available
  * Working
  * Maintenance
  * Inactive
* **CSV Export** of current inventory
* **CSV Import** to append new equipment records

### 🏗️ Work Assignments

* Assignment cards for each fleet number
* Displays:

  * Location
  * Customer
  * Supervisor
  * 1st & 2nd shift operator details
  * PF numbers and working hours

### 📈 Reports

* Summary KPIs:

  * Total equipment
  * Active equipment (with operator)
  * Total working hours
* Detailed per-fleet report table
* CSV export hook ready (table already rendered in UI)

### 🎨 UI / UX

* Dark / Light theme toggle (top-right)
* Collapsible sidebar (top-left) for more workspace
* Responsive layout (desktop & tablet friendly)

---

## 🛠️ Tech Stack

* **HTML5** – Single `index.html`
* **CSS3** – Flexbox, grid layout, custom dark theme
* **Vanilla JavaScript** – No frameworks or dependencies

---

## ⚡ Getting Started

1. Clone or download this repository
2. Open `index.html` directly in a browser
   **OR** serve using any static server:

   ```bash
   # Option 1
   npx serve

   # Option 2
   python -m http.server
   ```
3. No build step or installation required

---

## 🧩 Data Model

All views are driven by a single in-memory JavaScript array:

Whenever you:

* Add equipment via the modal
* Import a CSV file

The app automatically re-renders:

* Dashboard KPIs & status bar
* Recent activity list
* Inventory table
* Assignment cards
* Reports table & summary KPIs

---

## 📄 CSV Format

### Exported CSV Columns

```
S.No, Fleet Number, Description, Type, Make, Model, Year, Status, Location
```

### Import Rules

On import, each CSV row creates a new `equipmentData` entry with:

* fleetNumber
* description
* type
* make
* model
* year
* status
* location

Additional fields (customer, operators, hours) are defaulted and can be updated later using the **Add Equipment** form.

---

## ⌨️ Keyboard & UI Notes

* Collapse sidebar: Top-left icon button
* Toggle dark mode: Top-right theme button
* Close modal: Press **Esc** or click outside the dialog

---

### Screenshots:

<img width="1919" height="881" alt="Screenshot 2025-12-18 183708" src="https://github.com/user-attachments/assets/b0b12cc0-548a-470a-888a-e05af908dea5" />

<img width="1919" height="869" alt="Screenshot 2025-12-18 183723" src="https://github.com/user-attachments/assets/964217c9-4a60-4ad1-855f-457df3dc0ae8" />

<img width="1919" height="876" alt="Screenshot 2025-12-18 183736" src="https://github.com/user-attachments/assets/a749dce4-c930-4a87-9da5-19b3bbe93e77" />

<img width="1919" height="873" alt="Screenshot 2025-12-18 183748" src="https://github.com/user-attachments/assets/6df36d02-adde-44c0-9198-a16f80d04ff5" />

<img width="1918" height="875" alt="Screenshot 2025-12-18 183818" src="https://github.com/user-attachments/assets/b632b0a9-9bdc-4eb1-b542-34d8547193e1" />





## 🎯 Customization

You can easily customize:

* Theme colors and fonts in the `<style>` section
* Initial fleet data in the `equipmentData` array
* Layout and components directly in `index.html`

---

