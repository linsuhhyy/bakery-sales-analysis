# bakery-sales-analysis
Project Title: Exploring product performance, sales trends, and customer behavior in a French bakery dataset.

# Bakery Sales Analysis  

## Executive Summary  
This project analyzes two years of French bakery sales (~230k transactions) to uncover **what sells, when it sells, and what sells together**. Findings show that:  
- **COUPE bread** acts as a *traffic driver* (6.3% of sales, only 0.6% of revenue).  
- **Baguettes** are the *core product*, delivering both high volume and revenue.  
- **Late mornings (9–12, especially Sundays at 11:00)** generate the highest sales.  
- **Classic product pairings** (e.g., COUPE + Baguette, Croissant + Pain au Chocolat) reveal bundling opportunities.  
- **Seasonality is strong**, with spikes in January (Galette des Rois), December (holidays), and summer months (July–August).  

**Business takeaway:** Use COUPE as a lead-in product for upselling, anchor promotions around baguettes, optimize staffing for late mornings and holiday seasons, and design bundles around natural product pairings.  

---

## Research Questions  
1. What are the best-selling products?  
2. When are sales the highest (time of day, week, month)?  
3. Which products are frequently bought together?  
4. Are cheap items traffic drivers or revenue drivers?  
5. What is the overall revenue trend over time?  

---

## Methods  
- **Data Cleaning**: handled duplicates, removed zero-price transactions, fixed product names (`PLATPREPARE`, `ARTICLE 295`, `.`).  
- **Feature Engineering**: created revenue, timestamp, hour/day/month columns.  
- **Aggregations**: `groupby`, `resample` for weekly/monthly revenue.  
- **Analysis Techniques**:  
  - Best sellers (quantity & revenue)  
  - Peak sales by hour/day  
  - Market basket (product pairings)  
  - Cheap item vs revenue contribution  
  - Weekly/monthly revenue trends  
- **Visualizations**: bar charts, treemaps, heatmaps, line charts.  

---

## Key Insights  

### Products  
- **COUPE bread** → 22,629 units sold, but only ~€3,394 revenue (**6.3% of items vs 0.6% of revenue**) → a *traffic driver*.  
- **Baguettes** → 22,042 units, ~€20,471 revenue (**6.1% of items vs 3.7% of revenue**) → the bakery’s *core product*.  
- **Viennoiserie** → €4,253 from only 830 sales → *high value per unit*.  

### Timing  
- **Hourly peaks:** 9:00–12:00 dominate, with **11:00 (€111k)** the strongest hour overall.  
- **Day-of-week peaks:**  
  - **Sunday 11:00** (€29.6k) → strongest slot overall.  
  - **Saturday 11:00** (€17.9k).
  - Weekly peaks are typically in Week 1 and/or 2.
  - Weekday peaks cluster at **12:00 (lunch)**.  

### Product Pairings  
Top combinations:  
1. **COUPE + TRADITIONAL BAGUETTE** (6,116 transactions)  
2. **CROISSANT + PAIN AU CHOCOLAT** (5,394)  
3. **CROISSANT + BAGUETTE** (4,927)  
4. **PAIN AU CHOCOLAT + BAGUETTE** (4,205)  

*Insight:* customers naturally bundle bread-with-bread and pastries-with-pastries → opportunity to formalize bundles.  

### Seasonality  
- **January**: boost from Galette des Rois.  
- **December**: holiday pastries.  
- **Summer (July–August)**: highest revenues (€42k–€54k).  
- Revenue cools in September.  

---

## 💡 Business Recommendations  

1. **Leverage COUPE as a traffic driver**  
   - Extremely popular but low revenue.  
   - Bundle with higher-margin items (coffee, baguettes, pastries).  

2. **Protect and promote baguettes as the core product**  
   - Consistently high in both volume and revenue.  
   - Anchor promotions (“Buy 2 baguettes, get 1 pastry half price”).  

3. **Optimize staffing & production for peak hours**  
   - Sales peak 9–12, especially weekends.  
   - Increase staff and oven cycles during these hours.  

4. **Design bundles around natural pairings**  
   - CROISSANT + PAIN AU CHOCOLAT, COUPE + BAGUETTE.  
   - Offer “breakfast bundles” and “bread duos.”  

5. **Prepare for seasonal spikes**  
   - January, December, and the summer months drive revenue peaks, especially in the first 2 weeks of the month. 
   - Plan inventory, staffing, and promotions accordingly.  

6. **Upsell premium categories**  
   - Viennoiseries and confiseries generate strong revenue per unit.  
   - Feature prominently in displays and cross-sell with traffic drivers.  

---

## Example Visuals  

![Top Products Treemap]()  

![Hourly Sales Heatmap](images/hourly_heatmap.png)  

![Cheap Items: Quantity vs Revenue](images/cheap_items_qty_vs_rev.png)  

![Top Product Pairs](images/product_pairs.png)  

![Weekly Revenue Trend](images/weekly_revenue_trend.png)  

![Monthly Revenue Trend](images/monthly_revenue.png) 
