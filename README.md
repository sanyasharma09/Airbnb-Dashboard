# 🌍 Global Airbnb Performance Dashboard

### Power BI | DAX | Power Query | Data Modeling | Business Intelligence

An interactive three-page Power BI dashboard analyzing Airbnb market performance across 10 global cities, with a focus on listing growth, market concentration, pricing, guest ratings, review behavior, seasonality, and host trust.

---

## 📊 Dashboard Preview

### 1. Market Overview
![Overview Dashboard](images/overview.png)

### 2. Market & Ratings Analysis
![Ratings Dashboard](images/ratings.png)

### 3. Reviews, Seasonality & Trust
![Reviews Dashboard](images/reviews.png)

---

## 📌 Project Overview

The **Global Airbnb Performance Dashboard** analyzes **279K+ listings, 182K+ hosts, and 5M+ reviews across 10 global cities**.

The project transforms raw Airbnb listing and review data into business-focused insights using **Power Query, data modeling, DAX, KPI reporting, trend analysis, and interactive visualizations**.

The dashboard helps answer questions such as:

- Which cities contribute the largest share of Airbnb listings?
- How has listing activity changed over time?
- Which room types command the highest prices?
- Which cities perform best across guest-rating metrics?
- How frequently do customers leave reviews?
- How does review activity vary across months?
- What proportion of hosts provide identity and profile trust signals?

---

## 🎯 Business Objective

Airbnb operates across markets with significantly different listing volumes, pricing patterns, customer ratings, and host characteristics.

The objective of this project was to build an interactive analytical dashboard that enables users to:

- Track listing growth over time
- Compare city-level market performance
- Analyze pricing differences by room type
- Evaluate guest satisfaction across rating dimensions
- Understand review frequency and customer behavior
- Identify seasonal review patterns
- Measure host trust using verification indicators

---

## 🛠️ Tech Stack

- **Power BI Desktop** – Dashboard development and interactive reporting
- **Power Query** – Data cleaning, transformation, and preparation
- **DAX** – Calculated measures, KPIs, ranking, cumulative analysis, and percentage calculations
- **Data Modeling** – Relationship management between Listings and Reviews tables
- **Power BI Visuals** – KPI cards, ribbon charts, matrices, bar charts, line charts, and combination charts
- **File Format** – `.pbit` Power BI template and `.png` dashboard previews

---

## 📂 Dataset

**Dataset:** Airbnb Listings & Reviews  
**Source:** Maven Analytics Data Playground  
**Original Source:** Inside Airbnb

The dataset contains:

- **279K+ Listings**
- **182K+ Hosts**
- **5M+ Reviews**
- **10 Global Cities**
- **144 Property Types**

### Listings Table

Contains information such as:

- Listing ID
- Host ID
- City
- Property Type
- Room Type
- Price
- Host Superhost Status
- Host Identity Verification
- Host Profile Picture Status
- Guest Ratings
- Amenities

### Reviews Table

Contains:

- Listing ID
- Review ID
- Reviewer ID
- Review Date

The two tables are connected through **`listing_id`** to support cross-table analysis.

---

## 🔄 Analytics Workflow

**Raw Data → Power Query → Data Cleaning & Transformation → Data Modeling → DAX Measures → Exploratory Analysis → Dashboard Development → Business Insights**

Key tasks performed:

- Data type validation
- Data cleaning and transformation
- Date preparation for time-series analysis
- Table relationship creation
- DAX measure development
- KPI calculation
- Cumulative percentage analysis
- Reviewer frequency analysis
- Host trust segmentation
- Monthly review-share analysis
- Dashboard formatting and visual design

---

# 📈 Dashboard Walkthrough

## 1️⃣ Market Overview

The first dashboard page provides a high-level view of Airbnb's global scale and listing growth.

### Key KPIs

- **279,712 Listings**
- **182,024 Hosts**
- **10 Cities**
- **144 Property Types**
- **5M+ Reviews**

### Key Insight

Airbnb listing activity grew rapidly during its expansion phase and reached its highest level around **2015**, followed by slower growth and a sharp decline around the COVID-19 period.

---

## 2️⃣ Market, Pricing & Ratings Analysis

The second page compares market share, pricing, and guest satisfaction across cities.

### Market Share by City

A cumulative contribution analysis ranks cities by listing volume and compares:

- Superhost Listings
- Non-Superhost Listings
- Cumulative Share of Listings

### Key Insight

**Paris, New York, and Sydney account for nearly half of the listings and approximately 48% of total reviews**, showing strong market concentration in a small number of cities.

### Room-Type Pricing

Average price comparison:

| Room Type | Average Price |
|---|---:|
| Hotel Room | ~$800 |
| Entire Place | ~$673 |
| Shared Room | ~$580 |
| Private Room | ~$462 |

Hotel rooms recorded the highest average price, while private rooms represented the lowest-priced accommodation type.

### Guest Rating Analysis

Cities were compared across:

- Accuracy
- Cleanliness
- Communication
- Location
- Value

### Key Insight

**Mexico City and Rio de Janeiro recorded some of the strongest overall ratings**, while Hong Kong and Istanbul performed comparatively lower.

Cleanliness and value were among the relatively weaker-scoring rating dimensions.

---

## 3️⃣ Reviews, Seasonality & Host Trust

The third page focuses on customer review behavior and host credibility.

### Review Frequency Analysis

A cumulative frequency analysis was created to understand how frequently individual reviewers contribute reviews.

### Key Insight

Approximately **98.8% of reviewers submitted three reviews or fewer**, showing that most customer review activity comes from occasional reviewers.

A small number of unusually high-frequency reviewers were also identified as potential outliers.

### Review Seasonality

Monthly review share was analyzed across:

- Mexico City
- New York
- Paris
- Rome
- Sydney

### Key Insight

**Paris and Rome show stronger review activity from April to August**, reflecting stronger European summer travel activity.

**New York shows increased review activity in November and December**, corresponding with the holiday season.

> Review activity is used as an engagement indicator and should not be interpreted as actual booking or occupancy data.

### Host Trust Analysis

Hosts were segmented using:

- Identity Verification
- Profile Picture Availability

Four groups were analyzed:

- Verified + Profile Picture
- Verified + No Profile Picture
- Not Verified + Profile Picture
- Not Verified + No Profile Picture

### Key Insight

**66.9% of hosts were both identity verified and had a profile picture**, while only a very small proportion lacked both trust signals.

---

## 🧠 Key DAX Measures

Some of the custom measures developed include:

```DAX
Total Listings
Hosts Total
Total Reviews
Avg Price
Avg Rating
Superhost Listings
City Rank
Cumulative Listings
Cumulative %
Reviewers
Reviews per Reviewer
Cumulative Reviewers
% of Total Reviewers
% of Monthly Reviews
Verified_Profile
Verified_NoProfile
NotVerified_Profile
NotVerified_NoProfile
