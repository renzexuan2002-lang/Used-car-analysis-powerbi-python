# 🚗 Used Car Market — Exploratory Data Analysis

> **Data Source:** [Secondhand Car Market Hungary — Kaggle](https://www.kaggle.com/datasets/attilakiss/secondhand-car-market-data-parsing-dataset-v1/data)  
> **Data Cleaning:** Python (pandas)  
> **Visualization:** Power BI  

---

## 📋 Dataset Overview

| Metric | Value |
|--------|-------|
| Total Listings | 31,023 |
| Brands Covered | 102 |
| Price Range | 50,000 to 59,789,000 HUF |

The raw dataset was sourced from Kaggle, containing advertisement records from Hungary's largest second-hand car marketplace. Data cleaning was performed in **Python** using `pandas` — handling missing values, type conversions, feature engineering (e.g. `car_age`, `price_range`, `sell_rate`).

---

## 1. 🏆 Top 10 Brands by Number of Listings

![Top 10 Brands by Number of Listings](images/Top%2010%20Brands%20By%20number%20of%20Listings%20.png)

**Key Findings:**

- **VOLKSWAGEN (2,789), FORD (2,767), and OPEL (2,743)** lead the market with nearly identical listing counts
- The top 3 brands have very similar listing counts, with less than 50 cars difference between them.
- **BMW (2,618)** and **MERCEDES-BENZ (2,138)** rank 4th and 5th, showing strong second-hand activity even in the premium segment
- The top 10 is almost entirely European, reflecting the Hungarian market's preference for EU-manufactured vehicles

> 💡 **Takeaway:** The used car market is dominated by European brands, with German manufacturers making up most of the top positions.

---

## 2. 💰 Top 10 Brands by Average Listing Price

![Top 10 Average Listing Price by Brand](images/Top%2010%20Average%20Listing%20Price%20by%20Brand%20.png)

**Key Findings:**

- **MERCEDES-AMG (22.6M HUF)** and **TESLA (21.9M HUF)** are the only two brands averaging above 20M
- **MASERATI (12.2M)** and **FISKER (11.5M)** form the second tier, both above 10M
- **PORSCHE (10.5M), BENTLEY (9.8M), ROLLS-ROYCE (8.5M)** represent the classic European ultra-luxury segment
- **CADILLAC (8.1M), DS (7.9M), HUMMER (7.8M)** cluster closely around 8M

> 💡 **Takeaway:** EVs and traditional luxury brands are now on equal footing in the second-hand market. TESLA's 21.9M average is a strong signal of high resale value for electric vehicles.

---

## 3. 📦 Price Distribution of Cars

![Price Distribution of Cars](images/Price%20Distrbution%20of%20Cars%20.png)

**Key Findings:**

| Price Range | Count |
|-------------|-------|
| < 1M HUF | 7,960 |
| 1M – 2M HUF | 8,046 |
| 2M – 3M HUF | 6,828 |
| 3M – 5M HUF | 1,531 |
| 5M – 10M HUF | 4,660 |
| > 10M HUF | 1,998 |

- **1M–2M** is the most common price range with 8,046 listings
- The **3M–5M range has only 1,531 listings** — the fewest of any segment, even fewer than the >10M luxury tier
- Supply jumps back up in the 5M–10M range, suggesting a price skip driven by brand segmentation

> 💡 **Takeaway:** The 3M–5M price range shows unusually low supply, likely due to a structural gap between mainstream and premium vehicle segments.

---

## 4. 📉 Car Age vs. Average Price

![Car Age VS Price](images/Car_age%20VS%20Price%20.png)

**Key Findings:**

- **0–10 years:** Prices drop sharply from ~10M to under 2M — the steepest depreciation phase
- **10–30 years:** Prices flatten out and stay low, mostly under 1.5M HUF
- **30+ years:** A clear price recovery begins, with several data points reaching 5M–12M HUF — Maybe the classic/vintage car premium effect
- The 50–65 year range contains multiple high-value outliers, likely rare collectibles or restored vehicles

> 💡 **Takeaway:** Second-hand car prices follow a **U-shaped curve**. Cars experience the steepest depreciation within the first 10 years, while vehicles older than 30 years may gain value as collectible assets.

---

## 5. 🛣️ Mileage vs. Average Price

![Mileage VS Price](images/Mileage%20VS%20Price%20.png)

**Key Findings:**

- Low-mileage vehicles exhibit the widest price variation due to differences in brand and condition. As mileage increases, prices decline and converge, showing reduced variance. High-mileage vehicles are concentrated in the lower price range, while premium brands maintain high-value outliers across all mileage levels, indicating that brand strength can outweigh mileage in determining price.

> 💡 **Takeaway:** Mileage and price have a clear negative relationship — the higher the mileage, the lower and more predictable the price. For low-mileage cars, brand and condition matter far more than mileage alone.

---

## 6. ✅ Top 10 Brands by Sell Rate

![Top 10 Sell Rate by Brand](images/Top%2010%20Sell%20Rate%20by%20Brand%20.png)

**Key Findings:**

- **ZASTAVA (~75%)** has by far the highest sell rate
- **ISUZU (~57%) and MARUTI (~53%)** are the only other brands breaking the 55% mark
- Most top sell-rate brands belong to niche or discontinued segments, rather than mainstream manufacturers.
- High-volume mainstream brands are underrepresented in the top sell-rate rankings.

> 💡 **Takeaway:** The extremely high sell rate like ZASTAVA (3 out of 4 ) is heavily influenced by a very small sample size. With such a low denominator, the metric is highly volatile and not representative of stable market behavior.

## 🔍 Summary

| Dimension | Key Insight |
|-----------|-------------|
| **Market Structure** | European brands dominate the market, with German manufacturers accounting for 4 of the top 6 positions. |
| **Price Distribution** | The 1M–2M HUF range is the most common segment, while 3M–5M shows a structural supply gap. |
| **Depreciation Curve** |Vehicle prices follow a U-shaped pattern: steep depreciation within the first 10 years, followed by value recovery after 30 years. |
| **Mileage Impact** | Mileage is associated with a clear relationship with price, where higher mileage corresponds to lower and more stable price levels. |
| **Sell Rate** | Higher sell rates are generally associated with niche or low-supply brands, while mainstream brands experience lower turnover due to market saturation. |
| **EV Resale Value** | Tesla matches traditional luxury brands in average resale price |

---

## 🛠️ Tech Stack

```
Data Source   : Kaggle — Secondhand Car Market Hungary (attilakiss)
Data Cleaning : Python · pandas
Visualization : Power BI Desktop
```
