# E-Commerce Sales EDA — UK Online Retail Dataset

Exploratory Data Analysis on a UK-based e-commerce transactional dataset, uncovering revenue drivers, top markets, best-selling products, and seasonal/hourly sales patterns.

## 📌 Overview

This project analyzes transactional data from a UK online retailer to answer business-relevant questions such as which countries and products generate the most revenue, when customers buy the most, and what actually drives revenue — order size or price.

**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn (Jupyter Notebook)

## 📂 Dataset

- **Source:** UK Online Retail transactional dataset (`ecommerce.csv`)
- Contains invoice-level transactions: Invoice No, Description, Quantity, Invoice Date, Unit Price, Country, etc.
- No missing values in the raw dataset.
- `InvoiceDate` was converted to proper datetime, and a `Revenue` column (`Quantity × UnitPrice`) was engineered for analysis.

> Note: raw data is not included in this repo. See [`data/README.md`](data/README.md) for details on the source.

## 🔍 Analysis Workflow

1. **Data Understanding** — inspected structure, types, and missing values
2. **Descriptive Statistics** — checked distributions of `Quantity` and `UnitPrice`
3. **Outlier Detection** — boxplots to assess spread and extreme values
4. **Categorical Analysis** — transaction volume by country
5. **Feature Engineering** — datetime conversion, `Revenue`, `MonthName`, `Hour` columns
6. **Business Questions** — answered 6 targeted questions with visualizations
7. **Correlation Analysis** — heatmap + scatterplots to assess revenue drivers

## 💡 Key Findings

| Question | Finding |
|---|---|
| Which country generates the most revenue? | **United Kingdom** — dominates both transaction volume and revenue |
| Best-selling product (by quantity)? | **White Hanging Heart T-Light Holder** |
| Product with highest revenue? | **White Hanging Heart T-Light Holder** |
| Which month has the highest sales? | **November** — likely pre-holiday season demand |
| Peak transaction hour? | **12:00 (noon)** |
| What drives revenue more: Quantity or Price? | **Quantity** (corr. ≈ 0.79) far outweighs UnitPrice (corr. ≈ 0.09) |

**Business takeaway:** Revenue is driven primarily by purchase volume rather than item price — pricing changes alone are unlikely to move revenue much; strategies that increase basket size (bundling, promotions, cross-selling) would likely have more impact.

Outliers in `Quantity` and `UnitPrice` were reviewed but not removed, since in an e-commerce context they plausibly represent bulk buyers or premium products rather than data errors.

## 📊 Sample Visualizations

See the notebook for the full set of charts, including:
- Revenue by country (bar chart)
- Top 10 best-selling products
- Monthly sales trend
- Hourly transaction distribution
- Correlation heatmap (Quantity, UnitPrice, Revenue)

## 🗂 Repository Structure

```
ecommerce-eda-analysis/
├── data/
│   └── README.md          # dataset source & description
├── notebooks/
│   └── eccomerce_analysis.ipynb
├── requirements.txt
└── README.md
```

## ▶️ How to Run

```bash
git clone https://github.com/<your-username>/ecommerce-eda-analysis.git
cd ecommerce-eda-analysis
pip install -r requirements.txt
jupyter notebook notebooks/eccomerce_analysis.ipynb
```

## 👤 Author

**Zidane**
Portfolio: [nzidane.com](https://nzidane.com)
