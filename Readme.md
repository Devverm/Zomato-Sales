# 🍽️ Zomato Dashboard — Power BI Analytics Project

A comprehensive business intelligence dashboard built on Zomato's food delivery data, providing deep insights into restaurant performance, customer behaviour, sales trends, and city-wise distribution across India.

---

## 📁 Project Structure

```
Zomato-Dashboard-PowerBI/
├── food.xlsx            # Menu items and veg/non-veg classification
├── orders.xlsx          # Transaction-level order records
├── restaurant.xlsx      # Restaurant metadata (location, rating, cuisine)
├── users.xlsx           # Customer demographics and profile data
├── Images/              # Dashboard screenshots and visual assets
└── README.md
```

---

## 📊 Datasets Overview

### 1. `food.xlsx` — Menu Items (371,560 records)
| Column | Description |
|---|---|
| `f_id` | Unique food item identifier |
| `item` | Name of the dish |
| `veg_or_non_veg` | Classification: Veg / Non-Veg |

### 2. `orders.xlsx` — Order Transactions (150,281 records)
| Column | Description |
|---|---|
| `order_date` | Date the order was placed |
| `sales_qty` | Number of units ordered |
| `sales_amount` | Revenue in INR |
| `currency` | Currency (INR) |
| `user_id` | Reference to the customer |
| `r_id` | Reference to the restaurant |

### 3. `restaurant.xlsx` — Restaurant Information (148,540 records)
| Column | Description |
|---|---|
| `id` | Unique restaurant identifier |
| `name` | Restaurant name |
| `Country` | Country of operation |
| `city` | City where restaurant is located |
| `rating` | Average customer rating |
| `rating_count` | Number of ratings received |
| `cuisine` | Cuisine type(s) offered |
| `link` | Swiggy/Zomato listing URL |
| `address` | Physical address |

### 4. `users.xlsx` — Customer Profiles (100,000 records)
| Column | Description |
|---|---|
| `user_id` | Unique customer identifier |
| `name` | Customer name |
| `Age` | Customer age |
| `Gender` | Male / Female |
| `Marital Status` | Single / Married |
| `Occupation` | e.g., Student, Employee, Self-employed |

---

## 📈 Dashboard Pages

### Page 1 — Overview
A high-level snapshot of Zomato's operations:
- Total orders, revenue, quantity, and ratings at a glance
- Sales breakdown by food category (Veg, Non-Veg, Others)
- Year-over-year sales trend (2017–2020)
- City-wise order distribution

### Page 2 — User Dynamics
Insight into the customer base:
- Active vs. churned user analysis
- New users gained vs. users lost over time
- Demographic breakdown by age, gender, and occupation
- Marital status segmentation

### Page 3 — City-wise Analysis
Geographic deep-dive:
- Top performing cities by sales and order volume
- Rating distribution across cities
- Most active user bases by region

---

## 🔑 Key Metrics

| Metric | Value |
|---|---|
| Total Orders | 150,281 |
| Total Revenue | ₹987 million |
| Total Quantity Sold | ~2 million units |
| Restaurants Onboarded | 148,540 |
| Cities Served | 150,281+ locations |
| Registered Users | 100,000 |

---

## 📌 Key Insights

- **Top Cities:** Tirupati, Electronic City (Bengaluru), Baner (Pune), Raipur, and Malviya Nagar lead in order volumes.
- **Category Performance:**
  - Veg: ₹122 million in sales (highest category)
  - Non-Veg: ₹106 million in sales
  - Others: ₹24 million in sales
- **Sales Trend:**
  - 2018 was the peak year at ₹0.41 billion
  - 2019 saw a slight decline to ₹0.34 billion
  - 2020 dropped to ₹0.14 billion (likely COVID-19 impact)
- **Food Catalogue:** Over 371,000 menu items catalogued across restaurants.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard creation and data modelling |
| **Microsoft Excel / CSV** | Source data format |
| **DAX** | Custom measures and KPIs |
| **Power Query** | Data transformation and cleaning |

---

## 🚀 Getting Started

1. **Clone or download** this repository.
2. Open **Power BI Desktop**.
3. Load the four `.xlsx` files as data sources:
   - `food.xlsx`
   - `orders.xlsx`
   - `restaurant.xlsx`
   - `users.xlsx`
4. Set up relationships:
   - `orders[r_id]` → `restaurant[id]`
   - `orders[user_id]` → `users[user_id]`
5. Open the `.pbix` report file and refresh the data source paths if needed.
6. Explore the three dashboard pages using the built-in slicers and filters.

---

## 🔗 Data Relationships

```
users (user_id) ──────< orders (user_id)
                              │
restaurant (id) >──────── orders (r_id)
```

---

## 📷 Dashboard Preview

![Zomato Dashboard Preview](https://github.com/Ganeshkarwa/-The-Zomato-Dashboard-using-Power-BI-/assets/140792447/98c5b00f-c7ab-48c1-903b-5a5b064d4c0a)

---

## 📄 License

This project is created for educational and analytical purposes. Data is sourced from publicly available Zomato/Swiggy listings. Not intended for commercial use.

---

## 🙌 Acknowledgements

- Data sourced from the **Zomato API** and publicly available restaurant listings.
- Built with **Microsoft Power BI** for visualization and business intelligence.

---

*#PowerBI #DataAnalytics #ZomatoAnalysis #BusinessIntelligence #DataVisualization*
