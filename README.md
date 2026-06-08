# 🚗 Second-Hand Car Market — Exploratory Data Analysis

> **Data Source:** [Secondhand Car Market Hungary — Kaggle](https://www.kaggle.com/datasets/attilakiss/secondhand-car-market-data-parsing-dataset-v1/data)  
> **Data Cleaning:** Python (pandas)  
> **Visualization:** Power BI  

---

## 📋 Dataset Overview

| Metric | Value |
|--------|-------|
| Total Listings | 31,023 |
| Brands Covered | 102 |
| Price Range | < 1M to > 10M HUF |
| Top Sell-Rate Brand | ZASTAVA (~80%) |

The raw dataset was sourced from Kaggle, containing advertisement records scraped from Hungary's largest second-hand car marketplace. Data cleaning was performed in **Python** using `pandas` — handling missing values, type conversions, outlier flagging, and feature engineering (e.g. `car_age`, `price_range`, `sell_rate`).

---

## 1. 🏆 Top 10 Brands by Number of Listings

![Top 10 Brands by Number of Listings](images/Top%2010%20Brands%20By%20number%20of%20Listings%20.png)

**Key Findings:**

- **VOLKSWAGEN (2,789), FORD (2,767), and OPEL (2,743)** lead the market with nearly identical listing counts, indicating dominant and stable supply across all three
- The top 3 brands are separated by fewer than 50 listings — a remarkably tight race
- **BMW (2,618)** and **MERCEDES-BENZ (2,138)** rank 4th and 5th, showing strong second-hand activity even in the premium segment
- The top 10 is almost entirely European, reflecting the Hungarian market's preference for EU-manufactured vehicles
- Volkswagen Group brands (VW + AUDI + SKODA) account for 6,408 listings combined — the single largest group by manufacturer

> 💡 **Takeaway:** The market is dominated by European mass-market brands. VW Group holds the largest combined footprint, while German premium brands (BMW, Mercedes) maintain strong second-hand supply.

---

## 2. 💰 Top 10 Brands by Average Listing Price

![Top 10 Average Listing Price by Brand](images/Top%2010%20Average%20Listing%20Price%20by%20Brand%20.png)

**Key Findings:**

- **MERCEDES-AMG (22.6M HUF)** and **TESLA (21.9M HUF)** sit at the very top — the only two brands averaging above 20M
- **MASERATI (12.2M)** and **FISKER (11.5M)** form the second tier, both above 10M
- **PORSCHE (10.5M), BENTLEY (9.8M), ROLLS-ROYCE (8.5M)** represent the classic European ultra-luxury segment
- **CADILLAC (8.1M), DS (7.9M), HUMMER (7.8M)** cluster closely around 8M, forming a distinct third tier
- TESLA's near-top ranking confirms that electric luxury vehicles hold their value competitively against established ICE luxury marques

> 💡 **Takeaway:** EVs and traditional luxury brands are now on equal footing in the second-hand market. TESLA's 21.9M average is a strong signal of high resale value for electric vehicles.

---

## 3. 📦 Price Distribution of Cars

![Price Distribution of Cars](images/Price%20Distrbution%20of%20Cars%20.png)

**Key Findings:**

| Price Range | Count | Share |
|-------------|-------|-------|
| 1M – 2M HUF | 8.0K | Highest |
| < 1M HUF | 8.0K | Tied highest |
| 2M – 3M HUF | 6.8K | 3rd |
| 5M – 10M HUF | 4.7K | 4th |
| > 10M HUF | 2.0K | 5th |
| 3M – 5M HUF | 1.5K | Lowest |

- The sub-3M range accounts for roughly **73% of all listings** — the market is overwhelmingly mid-to-low price
- The **3M–5M range is a notable gap**, with the fewest listings of any segment — even fewer than the >10M luxury tier
- Supply jumps back up in the 5M–10M range, suggesting a price skip driven by brand segmentation

> 💡 **Takeaway:** The 3M–5M range is an anomalous low-supply pocket. This could indicate a natural brand gap between mainstream and premium, or a buyer preference cliff worth investigating further.

---

## 4. 📉 Car Age vs. Average Price

![Car Age VS Price](images/Car_age%20VS%20Price%20.png)

**Key Findings:**

- **0–10 years:** Prices drop sharply from ~10M to under 1M — the steepest depreciation phase
- **10–30 years:** Prices flatten out and stay low, mostly in the 0.5M–1.5M range
- **30+ years:** A clear price recovery begins, with several data points reaching 5M–12M HUF — the classic/vintage car premium effect
- The 50–65 year range contains multiple high-value outliers, likely rare collectibles or restored vehicles

> 💡 **Takeaway:** Second-hand car prices follow a **U-shaped curve** rather than a simple linear decline. The first 10 years bring the heaviest depreciation; cars older than 30 years begin appreciating as collectibles.

---

## 5. 🛣️ Mileage vs. Average Price

![Mileage VS Price](images/Mileage%20VS%20Price%20.png)

**Key Findings:**

- **Low mileage (0–50K km):** Prices are highly dispersed, ranging from near zero to 60M HUF — brand and condition matter most here
- As mileage increases, average price converges downward rapidly
- **Above 100K km:** The vast majority of listings fall below 5M HUF
- **Above 200K km:** Prices compress further to the 1M–2M range with minimal variance
- High-price outliers persist at all mileage levels, representing premium brands that retain value regardless

> 💡 **Takeaway:** 100,000 km is the key psychological threshold. Buyers heavily discount vehicles past this mark.

---

## 6. ✅ Top 10 Brands by Sell Rate

![Top 10 Sell Rate by Brand](images/Top%2010%20Sell%20Rate%20by%20Brand%20.png)

**Key Findings:**

- **ZASTAVA (~80%)** has by far the highest sell rate — listings rarely sit unsold
- **ISUZU (~57%) and MARUTI (~55%)** are the only other brands breaking the 55% mark
- Nearly all top-10 sell-rate brands are **niche, discontinued, or Eastern European** marques (ZASTAVA, TRABANT, YUGO, WARTBURG)
- Major mainstream brands (VW, BMW, Ford) do not appear despite dominating listing volume

> 💡 **Takeaway:** High sell rates among niche/discontinued brands likely reflect low listing volumes, collector demand, and realistic pricing. Mainstream brands face a supply-demand imbalance.

---

## 🔍 Summary

| Dimension | Key Insight |
|-----------|-------------|
| **Market Structure** | European brands dominate; VW Group holds the largest combined share |
| **Price Distribution** | 73% of listings are under 3M HUF; 3M–5M is an anomalous gap |
| **Depreciation Curve** | U-shaped — steepest in years 0–10, recovery begins after 30 years |
| **Mileage Impact** | 100K km is the critical depreciation threshold |
| **Sell Rate** | Niche/discontinued brands clear faster; mainstream brands face oversupply |
| **EV Resale Value** | Tesla matches traditional luxury brands in average resale price |

---

## 🛠️ Tech Stack

```
Data Source   : Kaggle — Secondhand Car Market Hungary (attilakiss)
Data Cleaning : Python · pandas
Visualization : Power BI Desktop
```
