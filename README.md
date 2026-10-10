Uber Ride Data Analysis & Predictive Modeling

Tools: IBM SPSS Modeler | Logistic Regression | K-Means Clustering | Kohonen Networks

Project Overview

This project analyzes Uber ride-booking data to explore booking outcomes, understand factors associated with cancellations, and identify customer segments based on ride and booking characteristics.

Developed as part of my B.Tech in Computer Science Engineering (AI & Data Science) at Arka Jain University, the project uses IBM SPSS Modeler to build three analytical models:

Logistic Regression: Predicts booking status and explores factors associated with booking outcomes.
K-Means Clustering: Groups records into clusters based on selected ride and booking attributes.
Kohonen Networks: Uses a self-organizing map approach to explore patterns and customer segments.

The project combines predictive modeling, unsupervised learning, data preparation, model evaluation, and business-oriented interpretation.

Project Objectives
Analyze booking data to understand completed and cancelled rides.
Investigate the relationship between booking outcomes and factors such as driver arrival time, ratings, booking value, and vehicle type.
Explore customer segments using ride distance, booking value, and vehicle-related attributes.
Compare different analytical approaches and interpret their outputs.
Translate analytical findings into potential business applications for ride-hailing services.
Dataset

Dataset: Uber Ride Analytics Dataset (2024)
File: ncr_ride_bookings.csv
Records: 150,000
Fields: 21

The dataset contains booking, customer, vehicle, and trip information.

Selected attributes include:

Ride Distance
Average Driver Arrival Time (Avg VTAT)
Trip Duration
Booking Value
Vehicle Type
Driver and Customer Ratings
Booking Status

Booking outcomes include completed rides and different unsuccessful booking statuses, such as customer cancellations, driver cancellations, driver unavailability, and incomplete trips.

Tools & Technologies
IBM SPSS Modeler
Logistic Regression
K-Means Clustering
Kohonen Networks / Self-Organizing Maps
Data preparation and transformation
Model evaluation and visualization
Analytical reporting and presentation
Methodology

The project follows the CRISP-DM framework:

Business Understanding: Identify the need to understand booking outcomes and customer behavior.
Data Understanding: Inspect the dataset using the Variable File and Data Audit nodes.
Data Preparation: Use Derive, Reclassify, Filter, and Type nodes to prepare fields and define modeling roles.
Modeling: Build a Logistic Regression model and two clustering models.
Evaluation: Examine predictive accuracy, cluster quality, and model outputs.
Interpretation: Relate the results to potential operational improvements and customer segmentation strategies.
Model 1: Logistic Regression

Objective: Predict booking status and investigate factors associated with completed and unsuccessful rides.

Workflow
Import the dataset into IBM SPSS Modeler.
Audit the data for quality issues and invalid or missing values.
Prepare and transform fields using Derive, Reclassify, Filter, and Type nodes.
Partition the data into 60% training and 40% testing.
Train the Logistic Regression model.
Review model predictions, probabilities, accuracy, and variable importance.
Results and Interpretation

The report records a predictive accuracy of 96.59% for the booking-status modeling exercise.

The analysis identified driver arrival time, ratings, and booking value among the factors associated with booking outcomes in the model.

An important modeling decision involved comparing a binary completed-versus-cancelled target with the more detailed Booking Status field. The binary version returned 100% accuracy in the reported experiment, but this result was not considered sufficiently informative for the project's business objective.

The detailed booking-status target was preferred because distinguishing different unsuccessful outcomes can be more useful for investigating operational issues.

Evaluation note: Accuracy alone does not establish model quality. Further evaluation should include a confusion matrix, per-class precision and recall, and checks for class imbalance and data leakage.

Model 2: K-Means Clustering

Objective: Explore groups of bookings or customers with similar ride and booking characteristics.

Selected Attributes
Ride Distance
Booking Value
Encoded Vehicle Type
Workflow
Prepare and select the relevant fields.
Encode vehicle types numerically.
Configure the input fields in IBM SPSS Modeler.
Build the K-Means clustering model.
Visualize the resulting clusters using a 3D plot.
Results and Interpretation

The report records a silhouette score of 0.5 for the K-Means model.

The resulting clusters were interpreted in terms of differences in ride distance, booking value, and vehicle preferences. Potential business applications include exploring high-value bookings, shorter trips, and longer-distance journeys.

The actual cluster profiles should be validated against the model output before assigning definitive segment labels.

Model 3: Kohonen Networks

Objective: Explore patterns in the data using a self-organizing map-based clustering approach.

Selected Attributes
Booking Value
Ride Distance
Additional fields configured in the model workflow
Workflow
Prepare the selected input attributes.
Configure the modeling roles.
Train the Kohonen model in IBM SPSS Modeler.
Visualize the segment assignments using a 2D plot.
Results and Interpretation

The report records a silhouette score of 0.5 for the Kohonen model.

The self-organizing map provides a two-dimensional representation of patterns in the selected data. Its outputs can complement the K-Means analysis by offering another way to explore similarities between records.

The model's practical value depends on examining the resulting clusters and validating what distinguishes each group.

Business Applications

The analyses suggest several potential applications:

Operational analysis: Investigate patterns associated with unsuccessful bookings.
Service improvement: Explore whether driver arrival times or vehicle categories are associated with booking outcomes.
Customer segmentation: Identify groups with different ride distances and booking values.
Marketing analysis: Develop hypotheses for targeted promotions and service personalization.
Decision support: Present model outputs in a form that can inform further business investigation.

These are potential applications of the analysis rather than measured improvements in Uber's actual operations.

Key Learnings
Building visual data-mining workflows in IBM SPSS Modeler.
Preparing and transforming data for predictive and clustering models.
Applying Logistic Regression to a booking-status prediction task.
Exploring unsupervised learning with K-Means and Kohonen Networks.
Interpreting model outputs in the context of business questions.
Recognizing why a high accuracy score does not necessarily make a model useful.
Repository Contents
Final (1).str — IBM SPSS Modeler project stream.
Kmeans_customer_segmentation.gm — K-Means model file.
Kohonen_customer_segmentation.gm — Kohonen model file.
uber data report.pdf — project report.
uber data presentation .pptx — project presentation.
Future Improvements
Evaluate classification performance using a confusion matrix and per-class metrics.
Investigate potential data leakage and target-label quality.
Standardize numerical features before distance-based clustering, where appropriate.
Validate cluster profiles and compare the usefulness of the clustering approaches.
Add charts, reproducible analysis, and a clearer explanation of the data preparation steps.
Project Details

Project Type: Academic Data Analytics & Machine Learning Project
Institution: Arka Jain University
Program: B.Tech CSE (AI & Data Science)
Primary Tool: IBM SPSS Modeler
