🍽️ Kitchen Prep Time (KPT) Optimization — Zomato Case Study
📌 Project Overview

This project focuses on improving Kitchen Prep Time (KPT) prediction in a large-scale food delivery ecosystem similar to Zomato.

Kitchen Prep Time (KPT) is the time taken by a restaurant to prepare an order after it is confirmed.

Inaccurate KPT predictions lead to:

Rider early arrival and idle time

Fluctuating Estimated Time of Arrival (ETA)

Increased order cancellations

Poor customer experience

Higher operational costs

This project builds a data-driven system to diagnose KPT inaccuracies and develop a machine learning model to improve prediction accuracy.

🎯 Why This Project Was Built

In large food delivery platforms:

Merchant-marked “Food Order Ready” signals are often biased.

The system cannot see full kitchen workload (dine-in + competitor orders).

Peak-hour overload causes systematic underestimation of prep time.

The existing prediction system relies heavily on noisy human signals.

This project shifts prediction from:

Manual marking
→
Operational intelligence using data signals

🧠 What Problem This Project Solves

This project addresses three major issues:

1️⃣ Signal Noise & Bias

Merchant-marked prep times are inconsistent and behavior-driven.

2️⃣ Hidden Kitchen Load

The system does not directly observe total kitchen pressure.

3️⃣ Non-Linear Overload Effects

Small increases in Active Order Count can cause large spikes in prep time.

The solution:

Diagnose error patterns

Segment high-risk operational scenarios

Build a machine learning regression model

Reduce dependency on biased merchant signals

🏗️ Project Structure

The project is divided into structured analytical steps:

Step 1 — Diagnosis

Measured error between Merchant Marked KPT and Actual KPT

Created:

Kitchen_Prep_Time_Error_Minutes

Absolute_Kitchen_Prep_Time_Error_Minutes

Quantified bias and overall inaccuracy

Step 2 — Segmentation Analysis

Identified high-risk segments:

Peak vs Non-Peak hours

High vs Low Active Order Count

Merchant reliability buckets

Cuisine complexity segments

This step helped locate where most prediction errors occur.

Step 3 — Root Cause Analysis

Identified key causes:

Merchant behavioral bias

Hidden workload

Capacity bottlenecks

Non-linear overload effects

Step 4 — Machine Learning Model

Built a Random Forest Regressor to predict:

Actual Kitchen Prep Time (Minutes)

Compared model performance against merchant baseline using:

Mean Absolute Error (MAE)

Root Mean Square Error (RMSE)

🤖 Machine Learning Approach
Target Variable

Actual Kitchen Prep Time (Minutes)

Key Feature Categories

Kitchen Load Signals

Active Order Count

Effective Kitchen Load

Ambient Rush Index

Rider Waiting Time

Capacity Signals

Kitchen Capacity

Load Ratio

Order Complexity

Cuisine Complexity

Item Count

Contextual Cart Complexity

Behavioral Signals

Past Food Order Ready Reliability Score

Model Used

Random Forest Regressor

Why?

Handles non-linear relationships

Captures interaction effects

Robust to noisy real-world data

📊 Key Outcomes

Reduced prediction error compared to merchant-marked KPT

Identified peak-hour overload as major error driver

Demonstrated that operational signals outperform manual marking

Built a scalable prediction framework

Business impact areas:

Reduced rider idle time

Improved ETA reliability

Lower cancellation rates

Better operational efficiency

🛠️ Tools & Technologies Used

Python

Pandas

NumPy

Scikit-learn

Seaborn

Matplotlib

Google Colab

ReportLab (for PDF documentation)
