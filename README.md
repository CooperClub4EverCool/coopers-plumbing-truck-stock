# Truck Stock Management System

A web-based inventory checkout and tracking application built for **Cooper's Plumbing & Air**. This tool allows technicians to record materials taken from the plumbing stock room, track inventory usage, generate analytics, and automatically email inventory reports.

---

## Features

### 📋 Material Order Form

* Technician sign-out tracking
* Department selection (Service / Install)
* Work order/job number tracking
* Searchable inventory catalog
* Quantity management
* Custom item entry
* Stock recommendation submissions

### 📦 Records Management

* View historical inventory records
* Search by technician
* Filter by month
* Filter by item
* Export records to CSV
* Email individual records

### 👷 Technician Breakdown

* Department-specific reporting
* Monthly usage summaries
* Technician activity tracking
* Item quantity breakdowns
* CSV export support

### 📊 Analytics Dashboard

* Total orders submitted
* Total items used
* Unique technician counts
* Restock recommendation tracking
* Top-used inventory items
* Most active technicians
* Monthly activity reporting

### 📬 Email Notifications

* EmailJS integration
* Configurable recipients
* Custom email templates
* Dynamic merge fields
* Live email preview

---

## Screens

* Order Entry
* Records
* Technician Breakdown
* Analytics
* Settings

---

## Technology Stack

### Frontend

* HTML5
* CSS3
* Vanilla JavaScript

### Integrations

* Google Apps Script
* Google Sheets
* EmailJS

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/truck-stock-system.git
cd truck-stock-system
```

### Run Locally

Simply open:

```text
Index.html
```

in any modern browser.

No build tools or package installation required.

---

## Google Sheets Setup

The application stores inventory records using a Google Apps Script web endpoint.

Replace:

```javascript
const SCRIPT_URL = 'https://script.google.com/macros/s/YOUR_SCRIPT_URL_HERE/exec';
```

with your deployed Apps Script URL.

### Suggested Sheet Columns

| Column      | Description          |
| ----------- | -------------------- |
| ID          | Unique Record ID     |
| Tech        | Technician Name      |
| Date        | Checkout Date        |
| Job         | Work Order Number    |
| Items       | Item Names           |
| Quantities  | Quantities           |
| Categories  | Inventory Categories |
| Recommended | Restock Suggestions  |
| Created At  | Timestamp            |
| Department  | Service or Install   |

---

## EmailJS Setup

Create an EmailJS account:

https://www.emailjs.com

Configure:

```javascript
const EMAILJS_PUBLIC_KEY  = 'YOUR_PUBLIC_KEY';
const EMAILJS_SERVICE_ID  = 'YOUR_SERVICE_ID';
const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID';
```

### Required Template Variables

```text
to_email
cc_email
subject
message
from_name
```

---

## Email Template Tokens

### Subject Tokens

```text
{{tech}}
{{date}}
{{dept}}
{{job}}
```

### Body Tokens

```text
{{tech}}
{{date}}
{{dept}}
{{job}}
{{items_list}}
{{items_count}}
{{recommended}}
{{divider}}
{{company}}
```

Example:

```text
Plumbing Material Order – {{tech}} – {{date}} ({{dept}})
```

---

## Inventory Categories

The application includes inventory management for:

* Toilet / Flush Components
* Supply Lines & Connectors
* Drains & Basket Strainers
* Hose Bibbs & Sillcocks
* Ball Valves
* Gas Components
* Water Heater Materials
* Angle Stops
* Copper Fittings
* Copper Pipe & Soldering
* CPVC Fittings
* PEX Pipe & Fittings
* PVC Schedule 40
* PVC DWV
* Clamps, Straps & Anchors
* Fernco Couplings
* Faucet Parts
* Sealants & Chemicals
* PRV Boxes

---

## Export Options

### Records Export

Exports:

```csv
ID
Tech
Department
Date
Job Number
Items
Quantities
Categories
Recommended
Timestamp
```

### Technician Breakdown Export

Exports:

```csv
Tech
Department
Month
Date
Item
Quantity
```

---

## Project Structure

```text
.
├── Index.html
├── README.md
└── assets/
```

---

## Security Recommendations

Before production deployment:

* Restrict Google Apps Script access
* Validate user input
* Protect EmailJS credentials
* Limit authorized domains
* Implement authentication if required

---

## Future Enhancements

* User authentication
* Inventory quantity tracking
* Low-stock alerts
* Purchase order integration
* Barcode scanning
* Mobile application support
* PDF reporting
* Cost analysis dashboards
* Multi-location inventory support

---

## License

This project is intended for internal use by Cooper's Plumbing & Air.

---

## Author

**Cooper's Plumbing & Air**

Inventory tracking and stock room management system designed to improve technician accountability, inventory visibility, and operational reporting.
