
# Dashboard: Extreme Fitness – Membership & Revenue Analytics
    


## 📊 Power BI Report Download

The report is provided in `.pbix` format and is designed to be opened using **Microsoft Power BI Desktop**.  
Please ensure you have Power BI Desktop installed to view and interact with the dashboard.

📎[Download Power BI File (PBIX)](https://github.com/sujithts31618-ui/Fitness/raw/main/Fitness_analysis.pbix)


## LinkedIn
📎 https://tinyurl.com/5dces984

## Problem Statement

Managing a fitness center involves tracking multiple aspects such as client memberships, revenue, trainer allocation, and payment behaviors. However, data is often scattered across different sources, making it difficult for management to monitor performance in real-time. Without a centralized view, it becomes challenging to identify active vs. inactive members, analyze revenue trends, understand membership distribution, and target the right audience with promotional campaigns. This lack of visibility limits informed decision-making and impacts both operational efficiency and business growth.


### Steps followed 

- Step 1 : Data Preparation: Collect gym data (clients, memberships, trainers, payments, revenue, demographics).
- Step 2 : Import Data into Power BI
- Step 3 : Load client details, membership types (Gold, Silver, Platinum), payment info, revenue, and trainer data.
- Step 4 : Create Calculated Measures  using (DAX).
- Step 5 : KPIs: Total Clients, Revenue, Active/Inactive Members, Trainers.
- Step 6 : Donut Chart: Membership type distribution.
- Step 7 : Pie Chart: Payment type after discount..
- Step 8 : Slicer: Gender, Units, Date Range, Age Group.
- Step 9 : Image & Branding: Fitness logo, workout image.

### DAX logics

- Total Clients = COUNTROWS(Clients)
- Num of Trainers = COUNTROWS(Trainers)
- Revenue = SUM ( Payments[AmountAfterDiscount] )
- Active Members =
CALCULATE (
    COUNTROWS ( Clients ),
    FILTER ( Clients, Clients[Status] = "Active" )
)
- Inactive Members =
CALCULATE (
    COUNTROWS ( Clients ),
    FILTER ( Clients, Clients[Status] = "Inactive" )
)
- Active Membership =
CALCULATE (
    COUNTROWS ( Membership ),
    FILTER ( Membership, Membership[Status] = "Active" )
)
- Inactive Membership =
CALCULATE (
    COUNTROWS ( Membership ),
    FILTER ( Membership, Membership[Status] = "Inactive" )
)
- Age Group =
SWITCH(
    TRUE(),
    Clients[Age] >= 15 && Clients[Age] <= 20, "15-20",
    Clients[Age] >= 21 && Clients[Age] <= 30, "21-30",
    Clients[Age] >= 31 && Clients[Age] <= 40, "31-40",
    Clients[Age] >= 41 && Clients[Age] <= 50, "41-50",
    Clients[Age] >= 51 && Clients[Age] <= 60, "51-60",
    "Other"
)



# Report Snapshot (Power BI DESKTOP) 
1.
![Dashboard](https://raw.githubusercontent.com/sujithts31618-ui/Fitness/main/Fit_1.png)


2.

![Dashboard](https://raw.githubusercontent.com/sujithts31618-ui/Fitness/main/Fit_2.png)


3.

![Dashboard](https://raw.githubusercontent.com/sujithts31618-ui/Fitness/main/Fit_3.png)

4.

![Dashboard](https://raw.githubusercontent.com/sujithts31618-ui/Fitness/main/Fit_4.png)

5.

![Dashboard](https://raw.githubusercontent.com/sujithts31618-ui/Fitness/main/Fit_5.png)

## 🎯 Outcome of the Dashboard

- The Fitness Dashboard provides a 360° view of Extreme Fitmess performance, enabling management to monitor client activity, membership trends, and financial performance in real time. It highlights total revenue, client engagement (active vs inactive), trainer availability, and membership distribution (Gold, Platinum, Silver).

- By analyzing age groups, gender, and payment patterns, the dashboard helps identify target segments for promotions, preferred payment methods, and client retention opportunities. This ensures data-driven decision-making for business growth.

## 👨‍💻 Author
*Dashboard Created By:* Sujith TS 

*Date:* 30th August 2025

## 📂 Download .pbix 
📊 [Download Power BI File (PBIX)](https://github.com/sujithts31618-ui/Fitness/raw/main/Fitness_analysis.pbix)

## 📌 Data Source Mockaroo web

