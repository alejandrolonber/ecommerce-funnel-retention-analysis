# E-commerce Conversion Funnel & User Retention Analysis (MercadoLibre Case Study)

## 📋 Project Overview
This project diagnoses user behavior, conversion drops, and user retention cycles for MercadoLibre across Latin American markets between January 1st and August 31st, 2025. Using advanced SQL aggregations and cohort matrices, the analysis uncovers structural friction points in the purchasing process and delivers strategic recommendations to maximize customer lifetime value (LTV).

## 🛠️ Tech Stack & Analytical Frameworks
* **Language & Tools:** SQL (PostgreSQL / BigQuery environment)
* **Frameworks Used:** * **Multi-stage Conversion Funnels:** Built utilizing Common Table Expressions (CTEs) to isolate user flow from product discovery to purchase.
  * **Cohort Analysis:** Developed behavioral matrices to track weekly user retention indicators (D7, D14, D21, D28) segmented by geography and registration period.

---

## 🧾 Executive Summary

### 🛒 1. Conversion Funnel Insights
* **The Critical Friction Point:** The most catastrophic user drop-off occurs between product selection (`select_item`: 76.90%) and adding the product to the cart (`add_to_cart`: 11.01%). **This represents a staggering 85.7% loss of potential buyers in a single step**, signaling a severe "intent vs. action" misalignment.
* **Regional Disparities:** * **Uruguay** leads the region with the highest conversion rate, securing a final purchase rate of **4.55%**.
  * **Mexico** follows with a healthy and stable flow, achieving a final conversion rate of **2.48%**.
  * **Paraguay, Colombia, and Ecuador** exhibit critical vulnerabilities, registering a **0% final purchase conversion rate** despite showing healthy user interaction volumes at the beginning of the funnel.

### 📉 2. Retention & Cohort Behavior
* **Short-Term Engagement vs. Long-Term Habit:** The platform demonstrates high efficacy in re-engaging users during their first week, maintaining an average Day 7 retention rate of **~86%**. However, it fails to turn this into a long-term habit, as retention sharply decays to **~2.5% by Day 28**.
* **Anomalous Drops:** The **August 2025 cohort** experienced an extreme collapse, crashing down to a **0.2% retention rate at D28**. This anomalies point toward major app performance issues, changes in logistics/shipping policies, or the conclusion of highly aggressive marketing incentives.
* **Geographical Leaders:** **Peru** leads long-term retention metrics at Day 28 with **3.2%**, whereas **Colombia** displays the lowest performance at **1.6%**.

---

## 💡 Strategic Recommendations

1. **Optimize the `select_item` to `add_to_cart` Interface:** Since the largest volume of users is lost right before adding items to the cart, resources should be prioritized here. Implementing single-click add-to-cart buttons, localized immediate shipping estimates, and upfront pricing transparency can reduce friction immediately.
2. **Audit Payment and Logistics Gateways for 0% Conversion Markets:** An urgent technical and operational review is required for Colombia, Ecuador, and Paraguay. A 0% checkout completion indicates systemic payment failures, uncompetitive international shipping fees, or severe checkout bugs.
3. **Investigation of the August Cohort:** Conduct a post-mortem review of the technological deployments and service terms active during August 2025 to isolate the cause of the customer retention collapse.
4. **Develop Habit-Loop Features:** Introduce gamified loyalty tiers, recurrent purchase subscriptions, or personalized multi-channel triggers (push notifications/coupons) around Day 10 to combat the severe decay observed between D7 and D14.

---

## 📊 Analytical Data Outputs

### General Conversion Funnel Performance
| Select Item % | Add to Cart % | Begin Checkout % | Add Shipping % | Add Payment % | Purchase % |
|---------------|---------------|------------------|----------------|---------------|------------|
| 76.90%        | 11.01%        | 4.00%            | 2.42%          | 2.09%         | 1.25%      |

### Cohort Retention Averages (Sample Trends)
| Cohort Group | Day 7 Retention | Day 14 Retention | Day 21 Retention | Day 28 Retention |
|--------------|-----------------|------------------|------------------|------------------|
| Normal Peak  | ~86.5%          | ~55.5%           | ~25.0%           | ~2.7%            |
| Aug-2025     | 70.8%           | 29.7%            | 7.5%             | 0.2%             |
