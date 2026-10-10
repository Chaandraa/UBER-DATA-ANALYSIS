# Uber Ride Data Analysis & Predictive Modeling 🚕📊

A data analytics and machine learning project focused on exploring Uber ride-booking outcomes, understanding cancellation drivers, and identifying customer segments using both supervised and unsupervised learning algorithms.

This repository contains the complete analytical workflow developed using **IBM SPSS Modeler** as part of the B.Tech Computer Science Engineering (AI & Data Science) curriculum at **Arka Jain University**.

---

## 🚀 Project Overview

This project implements the end-to-end **CRISP-DM framework** to analyze data from **150,000 Uber ride bookings**. By building and evaluating multiple statistical models, this analysis translates complex transactional data into actionable operational and marketing insights for ride-hailing services.

### 🎯 Project Objectives
* **Analyze Booking Trends**: Understand the core dynamics behind completed vs. unsuccessful rides.
* **Identify Attrition Drivers**: Evaluate how driver arrival times (Avg VTAT), ratings, and booking values impact cancellation rates.
* **Segment Customers**: Group users based on trip distances, vehicle selections, and spending patterns.
* **Evaluate Analytical Models**: Contrast different algorithmic approaches to optimize analytical reporting.

---

## 🛠️ Tools & Technologies

* **Primary Tool**: IBM SPSS Modeler
* **Methodology**: CRISP-DM Framework
* **Algorithms Implemented**:
  * Logistic Regression (Supervised Classification)
  * K-Means Clustering (Unsupervised Segmentation)
  * Kohonen Networks / Self-Organizing Maps (Neural Unsupervised Learning)

---

## 📊 Dataset Specifications

* **Dataset Name**: Uber Ride Analytics Dataset (2024)
* **File Name**: `ncr_ride_bookings.csv`
* **Volume**: 150,000 records | 21 structural fields
* **Key Attributes Utilized**:
  * `Ride Distance` & `Trip Duration`
  * `Average Driver Arrival Time (Avg VTAT)`
  * `Booking Value` & `Vehicle Type`
  * `Driver Rating` & `Customer Rating`
  * `Booking Status` *(Target variable: Completed, Customer Cancelled, Driver Cancelled, Driver Unavailable, Incomplete)*

---

## 🧠 Modeling Architecture & Workflows

### 1. Logistic Regression (Predictive Classification)
* **Objective**: Predict final booking status and isolate key operational variables driving cancellations.
* **Workflow**: Data Audit → Data Preparation *(Derive, Reclassify, Filter, Type nodes)* → Data Partitioning *(60% Train / 40% Test)*.
* **Performance**: Achieved a **96.59% predictive accuracy** using the detailed multi-class booking target. 
* **Key Insight**: A simplified binary model (Completed vs. Cancelled) yielded 100% accuracy due to target data leakage. The granular multi-class target was chosen instead to ensure actual business utility by mapping specific failure points.

### 2. K-Means Clustering (Customer Segmentation)
* **Objective**: Cluster similar customer journeys based on distance, spending, and fleet preference.
* **Inputs**: `Ride Distance`, `Booking Value`, `Encoded Vehicle Type`.
* **Performance**: Achieved a **Silhouette Score of 0.5**. Results were mapped into an exploratory 3D plot to separate high-value long journeys from short-distance economy trips.

### 3. Kohonen Networks (Self-Organizing Maps)
* **Objective**: Map complex high-dimensional customer patterns onto a simplified two-dimensional topological grid.
* **Inputs**: `Booking Value`, `Ride Distance`, and secondary workflow attributes.
* **Performance**: Achieved a **Silhouette Score of 0.5**. Provides an alternative, pattern-resilient topological overview that fills structural gaps left by traditional K-Means.

---

## 💼 Potential Business Applications

* **Operational Intelligence**: Deep-dive into specific driver/customer cancellation vectors to mitigate lost platform revenue.
* **Service Optimization**: Determine threshold limits for driver arrival times (`Avg VTAT`) before customer retention drops.
* **Targeted Marketing**: Deploy precision promotional campaigns tailored explicitly to high-value long-distance segments.

---

## 📈 Key Learnings

* Designed and deployed visual data-mining workflows inside **IBM SPSS Modeler**.
* Managed complex data preparation pipelines using conditional logic node operations.
* Formulated data partitioning strategies to validate classification models reliably.
* Discovered firsthand why generic **accuracy metrics can be misleading** without evaluating target labels, confusion matrices, and data leakage.

---

## 📦 Repository Contents

```text
├── Final (1).str                   # Core IBM SPSS Modeler project stream file
├── Kmeans_customer_segmentation.gm # Generated K-Means cluster model export
├── Kohonen_customer_segmentation.gm# Generated Kohonen SOM model export
├── uber data report.pdf            # Comprehensive academic project report
└── uber data presentation .pptx     # Executive summary project slide deck
```

---

## 🔮 Future Improvements
* **Advanced Evaluation Metrics**: Implement confusion matrices along with per-class precision, recall, and F1-scores.
* **Feature Engineering**: Standardize features prior to running distance-based algorithms to remove scaling bias.
* **Data Transparency**: Append programmatic scripts and visual charts to document data transformations explicitly.
