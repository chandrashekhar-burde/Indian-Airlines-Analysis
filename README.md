# ✈️ Indian Airlines Data Analysis | Power BI Project

An interactive Power BI dashboard analyzing Indian Airline performance across passenger traffic, profitability, customer experience and operational efficiency. The project transforms approximately 40K flight records into actionable business insights to support data-driven decision-making.

## 🎯 Business Objectives

- Which airline has the happiest customers?
- Which months are the busiest and slowest for flights?
- Which airlines carry the most passengers?
- Does carrying the most passengers guarantee the highest profit?
- Do customer complaints lower an airline's rating on different routes?
- Which months have the worst flight delays?
- Which airlines are the most punctual?
- Which airlines have the most baggage problems?

## 🛠️ Tools & Technologies

- **Power BI Desktop** – Dashboard development and visualization.
- **Power Query** – Data transformation and preparation.
- **Data Modeling** – Fact and dimension table relationships.
- **DAX** – KPI calculations and analytical measures.

## 📊 Dashboard Overview

The project consists of two pages of interactive report.

### 1. Traffic Performance

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/d2168e7c-1189-4be1-94df-21a17ffc7a93" />


**Key Business Insights:**
- Air India has the highest rating (**4.15/5**), while SpiceJet has the lowest (**3.62/5**).
- Travel is busiest in April and May (**2.25M** passengers) and slowest in August and September (**1.23M** passengers).
- IndiGo (**1.99M**) and Air India (**1.89M**) carry the most travelers, far ahead of smaller airlines like Star Air (**0.14M**).
- Out of **18.41bn** in total estimated profit, Air India captures the largest share at **61.60%**, more than doubling IndiGo's **23.48%** despite IndiGo carrying most passengers.

### 2. Operation Excellence

<img width="1536" height="864" alt="image" src="https://github.com/user-attachments/assets/cfe755ea-855d-4d3e-91ff-740421e12b2b" />


**Key Business Insights:**
- Routes with fewer complaints consistently earn higher customer ratings (above **4.2**), while routes with more complaints drop lower.
- Delays are worst in July (averaging **30.25 minutes**) and lowest in December (averaging **26.95 minutes**).
- IndiGo is the most on-time airline (**48.19%**), followed by Akasa Air (**42.44%**), while SpiceJet is the least punctual (**24.88%**).
- IndiGo has the largest share of baggage issues (**35.57%**), followed by Air India (**26.12%**) and SpiceJet (**20.2%**), whereas Star Air has the fewest (**6.84%**).

## 📁 Dataset & Data Model

**Dataset:**
- Approximately **40,000 flight records with 38 columns** in the main fact table.
- **5 records** in the dimension table to make dynamic image while slicing.


The dataset covers:
- Flight and aircraft information.
- Origin, destination and route details.
- Passenger capacity and load factors.
- Flight delays and cancellation information.
- Revenue, operating costs and estimated profit.
- Customer ratings, complaints and baggage issues.
- Fuel consumption, CO₂ emissions, etc.

**Data Model:** One-to-many relationship between the fact table and the dimension table.

## 🔍 KPI's or DAX Measures
```dax
Total Passenger = SUM(Flight_Data[Passengers])

Total Flights = COUNTROWS(Flight_Data)

Seat Capacity = SUM(Flight_Data[Seat_Capacity])

CO2 Per Passenger = DIVIDE(SUM(Flight_Data[CO2_Emissions_Tonnes_Est])*1000,SUM(Flight_Data[Passengers]),0)

Fuel Efficiency = DIVIDE(SUM(Flight_Data[Fuel_Used_Litres_Est])*100,SUM(Flight_Data[Distance_km]),0)

Avg Flight Duration = AVERAGE(Flight_Data[Flight_Duration_Min])

Avg Ticket Price = AVERAGE(Flight_Data[Average_Ticket_Fare_INR])

No. On-Time Flight = CALCULATE(COUNTROWS(Flight_Data), Flight_Data[On_Time_Flag] = 1)

No. Cancelled Flights = CALCULATE(COUNTROWS(Flight_Data), Flight_Data[Cancelled_Flag] = 1)

Flight Cancellation Rate = DIVIDE([No. Cancelled Flights], [Total Flights],0)
```

## 🎛️ Interactive Features

The dashboard includes interactive airline selection and slicers for:

- Route
- Destination City
- Origin Region
- Aircraft Type
- Dynamic Images


## 💡 Key Skills Used

- Data Cleaning & Transformation
- Data Modeling
- DAX & KPI Development
- Exploratory Data Analysis
- Business Problem Solving
- Data Visualization & Storytelling
- Interactive Dashboard Development

## 🚀 Project Presentation

Here is a short dashboard walkthrough demonstrating interactive filters, airline comparisons and report navigation:


https://github.com/user-attachments/assets/dbcaf872-e00e-4ec5-987e-f6d75a7a2ad6


## 👨‍💻 About Me

**Chandrashekhar Burde | Data Analyst**

While building real-world projects and exploring new ways to make data more valuable for businesses, my focus is not just on creating visualizations, but on understanding the story behind the data and translating it into actionable insights.

**Skills:** Power BI | Power Query | Excel/Google Spreadsheets | ETL/ELT | DAX | Data Modeling | Data Visualisation
