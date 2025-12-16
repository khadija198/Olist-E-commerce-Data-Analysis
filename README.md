# Olist: From Alarming Findings to Data-Driven Solutions
## 🌍 Available Languages
- 🇬🇧 English (this file)
- 🇫🇷 [Version française](README_FR.md)

## 📊 Introduction

This project was developed as part of the **final capstone project** of the **Le Wagon Data Analytics Bootcamp**, completed over a period of **three weeks**.

The objective of this project is to analyze the **Olist e-commerce dataset** in order to:

* Explore customer behavior
* Understand customer retention issues
* Generate meaningful, actionable insights

The project combines **data analysis, NLP, time-series forecasting, and business intelligence**, including:

* Natural Language Processing (NLP) for customer review analysis
* Order forecasting using **Prophet**
* Interactive dashboards built with **Power BI**

---

## Project Goals

The main goals of this project are to:

* Clean and prepare the dataset for analysis
* Use NLP techniques to understand the reasons behind low customer retention
* Apply Prophet to forecast order volumes over the next five years
* Build interactive and insightful dashboards using Power BI
* Provide clear, **data-driven recommendations** to improve Olist’s overall performance

---

## 🗂️ Dataset Overview

The Olist dataset is composed of [nine CSV files](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), each representing a different aspect of the e-commerce platform:

1. `olist_order_items_dataset`
2. `olist_orders_dataset`
3. `olist_order_payments_dataset`
4. `olist_order_reviews_dataset`
5. `olist_products_dataset`
6. `olist_customers_dataset`
7. `olist_sellers_dataset`
8. `olist_geolocation_dataset`
9. `olist_category_dataset`

---

## Data Dictionary

Olist provides a **comprehensive and well-structured data dictionary** that describes each variable across all tables.

This documentation [Data Dictionary.pdf](https://github.com/khadija198/Olist-E-commerce-Data-Analysis/blob/26cf8ed90bc9e5e86bd84980d66129e44f7eadd5/Data%20Dictionary.pdf)
:

* Explains the meaning and role of each feature
* Helps ensure correct interpretation of the data
* Facilitates navigation and understanding of relationships between tables

The data dictionary is essential for conducting accurate analyses and building reliable insights.

---

## Business Questions

### Global Performance

* What is the total revenue and how does it evolve over time?
* How many orders are received, and how does this change month by month?
* How many customers and sellers are active on the platform?
* Are orders delivered on time, or is there a high rate of late deliveries?
* What is the level of customer satisfaction (satisfied vs. unsatisfied)?
* Where are customers geographically located?

---

### Product Performance

* Which product categories generate the highest revenue?
* How many products are sold, and across how many categories?
* How do monthly order volumes change over time (2017 vs. 2018)?
* What is the average order value (AOV)?
* Which payment methods are most frequently used?
* How does revenue compare to the number of orders for each product category?

---

### Logistics Performance

* What is the average delivery time (ADT), and is it efficient?
* What percentage of orders are delivered on time (OTD)?
* What is the average transportation cost, and what factors influence it?
* How are operational times distributed (order approval, preparation, transportation)?
* Is there a correlation between product weight and transportation cost?
* Which states have the fastest and slowest delivery times?

---

## Customer Sentiment Analysis (NLP)

After exploratory analysis and dashboard creation, we observed that **customer retention was relatively low**.

To better understand the underlying reasons, we conducted a **sentiment analysis on customer reviews**, which is presented in the final dashboard.

This analysis highlights the main drivers of dissatisfaction, including:

* Product quality issues
* Delivery delays
* Customer service challenges

### Key Questions Addressed

* Which product categories receive the most negative reviews?
* What are the main reasons behind customer dissatisfaction?
* Which themes dominate negative feedback (product quality, delivery issues, customer service)?
* Which product categories are most affected by negative sentiment?

---

## Deliverables

* Cleaned and structured datasets
* Exploratory and analytical notebooks
* NLP sentiment analysis
* Time-series forecasting model
* Interactive Power BI dashboards


## 👥 Project Team

This project was developed as part of the Data Analytics & AI Bootcamp by:

- **Kawtar Jawda**  
- **Khadija Ait ouali**
- **Younes Oubella**
- **Mohammed Amine Regragui**


## 🛠️ Tech Stack
☁️ **Environment & Storage**

Google BigQuery – large-scale SQL storage and computation

Google Colab – Python notebook environment

🗄️ **Languages & Querying**

SQL – data exploration, transformations, duplicate checks, consistency analysis

📊 **Visualization & Reporting**

Power BI – interactive dashboards

Matplotlib / Seaborn – Python analytical charts

🐍 **Python & Data Science**

Python, NumPy, Pandas – cleaning, preprocessing, analysis

Scikit-learn – ML algorithms (classification, regression, clustering, LDA)

NLTK / spaCy – NLP preprocessing

Gensim – LDA Topic Modeling

🤖 **Models**

Prophet – forecasting future order volume

LDA – detection of the 3 main topics in negative customer reviews

Additional ML models – predictive and segmentation analyses

🔍 **Data Quality & Exploration**
✅ 1. Missing Values

For each table:

Missing value count

Percentage visualization

Cleaning strategy (drop, impute, correct)

Tables analyzed:
orders, order_items, customers, products, sellers, geolocation, reviews, payment

✅ 2. Column Types

Standardization of:

dates → datetime

identifiers → string

monetary fields → float

categories → categorical

✅ 3. Outlier Detection

Applied to:

payment_value

price

freight_value

delivery time metrics

✅ 4. Duplicate Detection

For each table:

Identification of duplicate records

Count of duplicates

Removal or consolidation

Tables concerned: same as above.

✅ 5. Order Timeline Analysis

Differences calculated between:

purchase → approval

approval → carrier pickup

pickup → delivery

actual vs. estimated delivery

Objective:

identify delivery delays

detect problematic orders

link delays with low ratings

❗ Missing Orders in order_items

Detection of orders with no associated items, indicating:

data entry issues

unlogged cancellations

potential KPI distortion

📈 Statistical Analysis & Correlations

Performed descriptive statistics and explored relationships between variables using:

correlation matrix (heatmap)

scatterplots

distribution analyses

Objectives:

detect key relationships between variables

understand drivers of delays, prices, and satisfaction

prepare data for modeling

📊 Dashboards & Insights
🟦 1. Global Dashboard

Provides a 360° view:

order volume over time

revenue trends

geographic distribution

delivery performance

overall satisfaction

🟩 2. Product Performance Dashboard

Covers:

top 5 best-selling categories

seasonality of orders

payment method distribution

🟧 3. Logistics Dashboard

Analyzes:

freight cost vs. product weight correlation

anomalies in order statuses

operational time distribution

delivery delays across Brazil

🟨 4. Customer Satisfaction Dashboard

Includes:

order distribution vs. review scores

best/worst sellers

categories driving dissatisfaction

rating distribution by region

🤖 5. Predictive Modeling

Using Prophet, the project forecasts order volume over the next five years, identifying seasonal peaks and long-term trends.

🧠 NLP Analysis – Topic Modeling (LDA)

We performed NLP on reviews with ratings ≤ 3, as well as the top 5 product categories with the most negative feedback.

LDA Model Configuration:

Algorithm: LDA (Latent Dirichlet Allocation)

n_components: 3 topics

Goal: Identify major themes among dissatisfied customers

Process: cleaning, tokenization, lemmatization, stopword removal

🎯 Strategic Business Recommendations

Based on product quality analysis, delivery performance, and NLP insights, several improvement levers were identified.

🔧 1. Issue: Poor Product Quality & Weak Customer Service

Customer reviews and the LDA model reveal major dissatisfaction factors:

poor product quality

slow customer support

frequent delivery delays

Recommended Actions
📝 A. Review contracts with low-performing sellers

High return rates

Frequent defective products

Poor customer ratings
→ Introduce a Seller Quality Index updated in real time

🤖 B. Deploy real-time AI Feedback Monitoring

Automatic NLP analysis of new reviews

Early detection of spikes in complaints

Live quality & CX dashboard

💬 C. Implement a 24/7 Customer Support Chatbot

Track orders

Provide return policies

Answer product questions
→ Faster response time, reduced workload

🚚 2. Issue: Delivery Delays & Product Unavailability

Analysis shows a strong negative impact of:

late deliveries

stockouts

Recommended Actions
📦 A. Short Term: Partial Outsourcing of Delivery

Use reliable logistics partners

Improve delivery speed and tracking

🏭 B. Mid/Long Term: Build a Centralized Logistics Hub

Faster shipment consolidation

Reduced transportation costs

📊 C. Smart Stock Planning with Deep Learning

Use LSTM/RNN/Prophet models to:

forecast demand

prevent stockouts

optimize inventory

✔ Impact

These combined recommendations can significantly improve:

customer satisfaction

product quality

logistics performance
