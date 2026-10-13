# 📊 Sales & Revenue Analytics Dashboard

[![Python Version](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.40+-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Plotly](https://img.shields.io/badge/Plotly-5.18+-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)](https://plotly.com/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

An executive-grade, interactive **Sales & Revenue Analytics Dashboard** built using **Python**, **Streamlit**, and **Plotly**. This application provides real-time financial tracking, profitability analysis, regional sales heatmaps, product leaderboard insights, and custom report exporting capabilities (CSV & Excel).

Designed with a sleek, dark-mode glassmorphic user interface to deliver actionable business intelligence for executives, sales managers, and financial analysts.

---

## 🚀 Project Overview

Modern businesses generate vast amounts of transactional data. This dashboard synthesizes raw sales records into intuitive visual analytics. It enables stakeholders to quickly identify top-performing product lines, spot low-margin orders, monitor regional revenue contributions, and analyze discount impacts on net profitability.

### Key Highlights
- **Real-Time KPI Tracking**: Total Sales Revenue, Total Net Profit, Order Volume, Average Order Value (AOV), and Net Profit Margin % with period-over-period baseline deltas.
- **Interactive Multi-Dimensional Filtering**: Filter by date range presets, geographic region, product category, sub-category, individual products, and customer segments.
- **Glassmorphism Dark UI**: Built with custom CSS to provide a clean, modern dashboard layout with glowing status indicators and hover elevation effects.
- **Custom Report Exporter**: Export filtered transactional data on demand in CSV or formatted Excel (`.xlsx`) format.

---

## ⚡ Features

### 1. 🎛️ Executive KPI Cards
- **Total Sales Revenue**: Overall revenue with period-over-period growth delta (`+X%`).
- **Total Net Profit**: Bottom-line profit with period-over-period growth delta (`+X%`).
- **Total Orders**: Total unique completed orders.
- **Average Order Value (AOV)**: Average revenue generated per order transaction.
- **Profit Margin (%)**: Overall net margin percentage with percentage-point change (`+X.X pts`).

### 2. 📊 Multi-Tab Visual Analytics (5 Interactive Tabs)
- **📈 Tab 1: Revenue Trends**: Monthly & quarterly revenue vs. profit dual-axis bar & line charts, category revenue share donut chart, and customer segment revenue matrix.
- **💰 Tab 2: Profitability & Margins**: Sales vs. profit bubble chart (size = quantity), discount rate impact curve on net margin, Category vs. Region profit margin heatmap, and automated low-margin order alerts (<10% margin).
- **🌍 Tab 3: Regional Performance**: Horizontal regional revenue comparison, top 10 global cities chart, and regional summary table.
- **🏆 Tab 4: Top Products**: Top 10 best-selling products revenue breakdown, units sold vs. profit margin matrix, and detailed leaderboard table.
- **📄 Tab 5: Data Explorer**: Full searchable dataframe viewer with column visibility controls and instant download buttons for **CSV** and **Excel (.xlsx)**.

---

## 🛠️ Technologies & Tools Used

- **Language**: Python 3.11+
- **Web Framework**: Streamlit (v1.30+)
- **Data Visualization**: Plotly Express & Plotly Graphic Objects
- **Data Manipulation**: Pandas & NumPy
- **Excel Generation**: OpenPyXL
- **Styling**: Custom CSS (Glassmorphism, CSS Grid, Flexbox)

---

## 📂 Dataset Description

The application includes an automated synthetic data engine ([data_generator.py](data_generator.py)) that produces a realistic 5,000-record sales transaction dataset saved to `data/sales_data.csv`.

| Field Name | Description | Example |
| :--- | :--- | :--- |
| `Order ID` | Unique transaction identifier | `ORD-2025-01587` |
| `Order Date` | Transaction date timestamp | `2025-06-15` |
| `Year / Month / Quarter` | Aggregation periods | `2025`, `2025-06`, `2025-Q2` |
| `Customer Type` | Market segment | `Corporate`, `Small Business`, `Consumer` |
| `Region / Country / City` | Geographic hierarchy | `North America` -> `United States` -> `Seattle` |
| `Category / Sub-Category` | Product taxonomy | `Electronics` -> `Laptops & Computers` |
| `Product Name` | Product title | `ProBook Workstation 16-inch` |
| `Unit Price / Unit Cost` | Financial cost structure | `$1,899.00` / `$1,101.42` |
| `Quantity` | Units purchased per order | `5` |
| `Gross Sales` | Pre-discount total | `$9,495.00` |
| `Discount % / Amount` | Applied promotional discount | `10.0%` / `$949.50` |
| `Sales Revenue` | Net revenue realized | `$8,545.50` |
| `Profit / Margin %` | Net profit and margin percentage | `$3,038.40` / `35.56%` |
| `Payment / Status` | Method and shipping status | `Bank Transfer` / `Delivered` |

---

## 🏗️ Project Structure

```text
SALES REVENUE DASHBOARD/
│
├── app.py                # Main Streamlit dashboard application
├── data_generator.py     # Synthetic sales dataset generator module
├── utils.py              # Data caching, filter logic, & KPI calculator
├── styles.py             # Glassmorphism CSS design system & Plotly visual themes
├── requirements.txt      # Required Python dependencies
├── .gitignore            # Git exclusion rules
├── README.md             # Project documentation
└── data/
    └── sales_data.csv    # Transactional dataset (auto-generated if missing)
```

---

## 📦 How to Run the Project Locally

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
cd "SALES REVENUE DASHBOARD"
```

### 2. Set Up a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Launch the Streamlit Dashboard
```bash
streamlit run app.py
```

The app will open automatically in your browser at `http://localhost:8501`.

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
