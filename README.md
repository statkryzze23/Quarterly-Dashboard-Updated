# 📊 Quarterly Sales Dashboard

An executive-level sales performance dashboard built with HTML, JavaScript, and Plotly. Tracks store-level sales metrics against brand averages across quarters and years.

## 🔗 Live Demo

👉 [View Dashboard](https://statkryzze23.github.io/Quarterly-Dashboard-Updated/)

---

## 📸 Features

- **KPI Cards** — Total Sales, Sales vs Brand Avg, Orders vs Brand Avg, Avg Ticket, Online Mix, and 3rd Party Mix, all benchmarked against the brand average for the selected period
- **Quick Insights Strip** — At-a-glance performance summary with positive/negative indicators
- **Sales by Order Type** — Donut chart breaking down Delivery, Dine In, To Go, and Pick Up mix
- **Online & 3rd Party Mix Trends** — Line charts comparing store vs brand average over time
- **Discount Trend** — Bar + line combo showing discount dollars and discount percentage by period
- **Average Ticket Trend** — Store vs brand average ticket over time
- **Quarterly Sales Trend** — Store revenue vs brand average over time
- **Store Ranking** — Top 10 / Bottom 10 toggle showing best and worst performing stores for the selected period, with brand average reference line

---

## 🔍 Filters

| Filter | Description |
|--------|-------------|
| **Store** | View a single store or all stores |
| **Year** | Filter by fiscal year |
| **Quarter** | Filter by quarter (Q1–Q4) |

> Brand averages always reflect the same year/quarter window as the selected filter — not all-time averages.

---

## 🗂️ File Structure

```
Quarterly-Dashboard-Updated/
├── index.html              # Dashboard application
└── quartersales_clean.csv  # Sales data source
```

---

## 🛠️ Built With

- [Plotly.js](https://plotly.com/javascript/) — Interactive charts
- [PapaParse](https://www.papaparse.com/) — CSV parsing
- [Google Fonts](https://fonts.google.com/) — DM Sans & DM Mono
- Vanilla HTML / CSS / JavaScript — No frameworks, no build step

---

## 🚀 Running Locally

Because the dashboard fetches the CSV file via a relative URL, you need a local server — simply opening `index.html` in a browser won't work.

**Option 1 — Python (quickest)**
```bash
python3 -m http.server 8000
```
Then open `http://localhost:8000` in your browser.

**Option 2 — VS Code**
Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension, right-click `index.html` → *Open with Live Server*.

---

## 📄 Data Format

The dashboard expects a CSV file named `quartersales_clean.csv` with the following key columns:

| Column | Description |
|--------|-------------|
| `store` | Store name |
| `year` | Fiscal year |
| `quarter_label` | Quarter label (e.g. Q1, Q2) |
| `period` | Period label for trend charts |
| `net_sales_total` | Total net sales |
| `number_orders_total` | Total order count |
| `ticket_average` | Average ticket size |
| `delivery_sales` | Delivery channel sales |
| `dine_in_sales` | Dine-in channel sales |
| `to_go_sales` | To-go channel sales |
| `pick_up_sales` | Pick-up channel sales |
| `web_app_net_sales_online` | Online/app sales |
| `x3rd_party_sales_total` | Third-party delivery sales |
| `discounts` | Total discount dollars |
| `percent_discount` | Discount as % of sales |
