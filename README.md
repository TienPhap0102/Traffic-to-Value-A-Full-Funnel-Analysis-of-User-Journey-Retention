# **TRAFFIC TO VALUE: A FULL FUNNEL ANALYSIS OF USER JOURNEY RETENTION**

## 📖 **Project Overview**

**The Business Context**

In an e-commerce landscape where Customer Acquisition Cost (CAC) is increasingly expensive, merely tracking website traffic or total orders is no longer sufficient to evaluate business performance. A significant portion of the marketing budget might be wasted on traffic sources with high drop-off rates or on acquiring one-time buyers. Marketing and commercial teams must clearly understand the "flow of customers from the advertising source to the final purchase" to optimize Return on Investment (ROI).

**The Core Objective**
The primary objectives are to:

* **Identify Funnel Bottlenecks:** Trace the customer flow from the marketing source to the first touchpoint, and ultimately to the purchased product or abandonment.

* **Optimize Marketing ROI:** Evaluate which acquisition channels bring in the highest quality traffic and which website landing pages cause the most severe customer drop-offs.

* **Enhance Cross-Device Conversion:** Compare user journeys across Mobile and Desktop platforms to identify device-specific friction points

## 🗄️ **Data Architecture & Tech Stack**

**The Dataset**

The analysis is built on a robust relational dataset encompassing daily e-commerce web traffic and transactional operations. The schema consists of six primary tables merged to create an end-to-end view:

* **Sessions:** Web traffic origins and device_type.
  
* **Pageviews:** Detailed navigation logs and timestamps across landing pages and product pages.  

* **Orders & Order Items:** Transactional facts, primary products purchased, revenue, and cost.  

* **Products:** Catalog dimensions including product names.  

* **Refunds:** Financial tracking for returned orders

**Can reach Data Dictionary**: [Here]

**The Tech Stack**

- **Language**: Python 3.x
- **Environment**: Google Colab / Jupyter Notebook.
- **Data Manipulation**: `pandas`, `numpy` (Advanced aggregation, merging, and cumulative calculations).
- **Data Visualization**: `plotly.express`, `seaborn`, `matplotlib`, `plotly.graph_objects`

## 🏆 **Executive Results & Strategic Recommendations**

### 📱 **Device-Specific Funnel Optimization**

The Sankey flow analysis segmented the user base into Mobile and Desktop groups, revealing stark contrasts in browsing behavior and conversion friction.

* **Desktop Group:** Desktop users tend to explore a wider variety of landing pages (`/home`, `/lander-2`, `/lander-5`) and demonstrate a higher overall conversion rate. However, `/lander-2` acts as a massive bottleneck, seeing **125K visits** but leading to massive drop-offs.

→ **Conduct a rigorous UI/UX audit** and **A/B testing** on /lander-2. Re-evaluate the product presentation, load speeds, and call-to-action (CTA) visibility on this specific desktop page.

* **Mobile Group:** Mobile traffic is heavily concentrated on fewer pages, primarily /home and `/lander-2`. The drop-off rate here is disproportionately high immediately after landing.

→ Implement a mobile-first redesign for `/lander-2`. Streamline the checkout flow to require fewer clicks, prioritize mobile payment integrations (Apple Pay, Google Pay), and ensure above-the-fold content hooks mobile users instantly.

### 🎯 **Traffic Source & End-to-End Conversion Rate**

The end-to-end journey mapping categorized every session into three ultimate statuses: Completed (30,590), Refunded (1,731), or Drop-off (440,558).

* **The Acquisition Engine:** gsearch completely dominates as the primary traffic driver across both nonbrand and brand campaigns.

* **The Drop-off Crisis:** An overwhelming **~93% of sessions** end in a **Drop-off** state without a purchase.

→ Shift marketing focus from pure top-of-funnel acquisition to middle-of-funnel Conversion Rate Optimization. Implement automated retargeting campaigns specifically targeting users who bounced after viewing a product page.

### 📦 **Product Portfolio Performance**

* The Hero Product **The Original Mr. Fuzzy** is the undisputed top-performing product, securing the vast majority of completed orders.

→ Leverage this proven product-market fit. Prominently feature **The Original Mr. Fuzzy** immediately on high-traffic, high-bounce landing pages like `/home` and `/lander-2` to capture attention early. Bundle this item with slower-moving inventory to increase Average Order Value.

## 📂 **Repository Structure**

├── dataset/                          # Dataset files (if applicable)

├── Sankey_Flow_Analysis.ipynb        # Main analysis notebook

└── README.md                         # Project documentation
