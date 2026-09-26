# Delhi-Metro-PowerBI-Analytics
Interactive Delhi Metro analytics dashboard built using Power BI, Power Query and DAX.
# Delhi Metro Trip & Profitability Analysis using Power BI

## About the Project

This project is a Power BI dashboard created using Delhi Metro trip data from 2022–2024. The main aim of the project was to understand passenger demand, revenue, profit, ticket type performance, and route-wise activity.

I worked on the dataset using Power Query before creating the dashboard. The project helped me practice data cleaning, data transformation, DAX, and data visualization in Power BI.

## Dataset

The dataset contains around 150,000 trip records from 2022 to 2024.

Some of the important columns include:

* Trip ID
* Date
* From Station
* To Station
* Passengers
* Ticket Type
* Fare
* Cost per Passenger
* Profit
* Profit per Customer
* Remarks

## Data Cleaning and Preprocessing

I used Power Query to prepare the raw dataset for analysis.

The main preprocessing steps were:

* Split the original combined data into separate columns.
* Changed the columns to their appropriate data types.
* Converted Date to Date format.
* Converted Passengers to Whole Number.
* Converted Fare, Cost per Passenger, Profit and Profit per Customer to Decimal Number.
* Checked missing values in Passengers, Ticket Type and Remarks.
* Checked negative values in Profit and Profit per Customer.
* Created a new `Route` column by combining From Station and To Station.
* Created `Total Revenue` using Fare × Passengers.

The cleaned data was then used for creating the Power BI visuals.

## DAX Measures

I created the following measures for the dashboard:

```DAX
Total Revenue =
SUMX(
    'Worksheet',
    'Worksheet'[Fare] * 'Worksheet'[Passengers]
)
```

```DAX
Total Profit =
SUM('Worksheet'[Profit])
```

```DAX
Total Passengers =
SUM('Worksheet'[Passengers])
```

These measures were used in the KPI cards and different visuals in the dashboard.

## Dashboard

The dashboard focuses mainly on:

* Total Revenue
* Total Profit
* Total Passengers
* Profit and passenger volume by ticket type
* Monthly revenue and profit trends
* Top 10 busiest routes
* Route-wise passenger activity
* Ticket type performance

The dashboard is designed so that the user can interact with the data using filters and explore different aspects of the metro trips.

## Key Questions Explored

Some of the questions I tried to answer through the dashboard were:

* Which routes have the highest passenger volume?
* How does passenger volume vary between ticket types?
* Which ticket types contribute more to profit?
* How does revenue change over the months?
* How does profit change over time?
* Which routes have the highest demand?

## Tools Used

* Power BI
* Power Query
* DAX
* Microsoft Excel

## Project Workflow

```text
Raw Dataset
     ↓
Data Import
     ↓
Power Query
     ↓
Data Cleaning & Transformation
     ↓
Calculated Columns
     ↓
DAX Measures
     ↓
Data Visualization
     ↓
Power BI Dashboard
```

## What I Learned

Through this project, I got hands-on practice with Power Query for data cleaning and transformation, DAX for creating measures, and Power BI for building an interactive dashboard.

It also helped me understand how raw data can be converted into a dashboard that makes it easier to identify patterns and compare different aspects of a dataset.

## Author

**Gopika Sureshkumar**

Aspiring Data Analyst / Data Scientist

Skills used in this project: Power BI | Power Query | DAX | Excel | Data Cleaning | Data Visualization

