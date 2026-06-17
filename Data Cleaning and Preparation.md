# README: Data Cleaning and Preparation 
⬅️ [Back to Business Performance Insights Report](README.md)

---

## Project Overview
This repository documents the data preparation pipeline for an **Electronics Sales Performance** dataset. The original data was delivered as a flat CSV file containing mixed currencies, formatting inconsistencies, and missing data points. 

The objective of this process was to clean, harmonize, and structure the raw dataset using Power BI (Power Query) so it could accurately feed the final analytics dashboard.

---

## Data Cleaning & Transformation Steps

The data preparation phase focused on data integrity, standardization, and ensuring all metrics were completely accurate before building any visuals.

### 1. Data Cleaning & Harmonization
* **Handling Missing Values:** Conducted an initial profile of the dataset to find empty cells. Missing fields in critical text columns (like product categories) were filled using contextual defaults, and missing numeric fields were resolved so they wouldn't skew our final sales totals.
* **Text & Date Standardization:** Cleaned up text columns by removing accidental spaces and fixing inconsistent capitalization. Date fields were transformed from raw text into a uniform date format to allow for accurate chronological tracking.

### 2. Currency Standardization (CAD to USD)
The raw dataset tracked transactions in both United States Dollars (**USD**) and Canadian Dollars (**CAD**). 
* To make sure the charts added up correctly, everything needed to be in a single currency.
* All Canadian Dollar transactions were isolated and converted into USD using a consistent historical exchange rate factor. 
* The final dataset reflects all financial metrics—including Revenue, Average Order Value (AOV), and Profit—exclusively in standard **USD ($)**.

### 3. Structural Breakdown
To make the data easier to manage within Power BI, the original flat file was organized into dedicated tables grouped by business logic:
* **Sales Data:** Holds the core numbers like order IDs, quantities, revenues, and profits.
* **Products & Categories:** Groups items by their names and classifications (Electronics, Home Appliances, Computers).
* **Customers & Locations:** Organizes buyer profiles along with their respective cities and countries.
* **Sales Representatives & Payment Contexts:** Tracks who made the sale and how the customer paid.

---

## Technical Environment
* **Data Source:** Raw CSV Transaction Log
* **Transformation Tool:** Power BI / Power Query
* **Final Output:** Interactive Electronics Sales Performance Dashboard
