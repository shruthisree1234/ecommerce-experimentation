# 📊 E-Commerce Conversion & Product Discovery A/B Test

### End-to-End Experiment Analysis: Segmentation, Statistical Testing & Executive Dashboard

---

## 🎯 Business Problem

An e-commerce platform observed **declining conversion rates** (orders per active user). The product team hypothesized that improving **product discovery** by surfacing more long-tail categories would increase user engagement and orders.

**Questions to Answer:**
1. Where do users drop off in the behavioral funnel?
2. Does the proposed discovery change increase orders per user?
3. Should we ship this feature?

---

## 📦 Dataset

- **Source:** Instacart-style transactional dataset (2017)
- **Size:** 3.4M orders, 22.5M line items, 206K users
- **Key Tables:** `orders`, `order_products`, `products`, `departments`

---

## 🔬 Methodology

### 1. Data Preparation & Feature Engineering
- Cleaned and joined 4 tables to create user-level and order-level features
- Engineered behavioral metrics:
  - Order frequency
  - Basket size
  - Reorder rate
  - Department preferences

### 2. User Segmentation
- Created **activity tiers** (High/Medium/Low) based on order frequency
- **Key Finding:** High-activity users (31%) generate **6.6x more value** than low-activity users

### 3. Funnel Analysis
- Segmented users into 10 order buckets (cohorts) based on order history
- Tracked engagement growth: **2.0 → 20.17 orders per user** from first to 42nd order
- **Retention reaches 100% after 2nd order**

### 4. A/B Test Design
- **Groups:** Control vs. Treatment (50/50 split)
- **Metric:** Orders per user (conversion proxy)
- **Statistical Test:** Two-proportion z-test

---

## 📊 Key Findings

### ✅ User Segmentation Insights:
- **High-activity users (31%):** 35 orders/user (drive 68% of orders)
- **Medium-activity users (25%):** 11 orders/user
- **Low-activity users (44%):** 5 orders/user

### ❌ Experiment Result: No Lift Detected
- **Control:** 16.60 orders/user
- **Treatment:** 16.58 orders/user
- **Lift:** -0.08% (p-value > 0.05, **not statistically significant**)

### 💡 Additional Insights:
- **Produce & Dairy drive 40% of orders**
- User engagement grows **10x from first to 42nd order**
- Retention stabilizes at 100% after 2nd order

---

## 🎯 Recommendation

**DO NOT SHIP** the current discovery experience.

**Instead, focus on:**
1. **Target high-value segments:** Optimize onboarding for high-activity users
2. **Optimize 2nd order milestone:** Drive users to their 2nd order (100% retention threshold)
3. **Department-specific discovery:** Focus improvements on Produce & Dairy (40% of orders)

---

## 🛠️ Technical Stack

| **Tool** | **Purpose** |
|----------|-------------|
| **Python** | Data cleaning, feature engineering, statistical analysis |
| **pandas** | Data manipulation and aggregation |
| **statsmodels** | Two-proportion z-test for A/B testing |
| **Tableau Public** | Executive dashboard and visualization |
| **Google Colab** | Development environment |

---

## 📈 Dashboard

🔗 **[View Interactive Tableau Dashboard](https://public.tableau.com/app/profile/shruthi.sree.thirunavukkarasu/viz/InstacartGrowthEngineSegmentationExperimentAnalysis/InstacartGrowthEngineSegmentationExperimentAnalysis)**

**Dashboard Features:**
- Executive KPI summary (206K users, 3.42M orders, -0.08% lift)
- User segmentation by activity tier
- Funnel growth visualization (10x engagement increase)
- Retention curve analysis
- Department performance breakdown

![Dashboard Preview](https://public.tableau.com/static/images/In/InstacartGrowthEngineSegmentationExperimentAnalysis/InstacartGrowthEngineSegmentationExperimentAnalysis/1.png)

---

## 📂 Repository Structure

