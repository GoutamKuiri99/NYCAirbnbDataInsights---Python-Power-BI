# NYC Airbnb Analysis: Insights with Python and Power BI

## Overview: 
Airbnb, Inc. is a leading American company that operates a prominent online marketplace for lodging, primarily focusing on vacation rentals and unique accommodations.

>- **Founded:** 2008
>- **Headquarters:** San Francisco, California
>- **Business Model:**
>>- Airbnb facilitates bookings through its website and mobile app.
>>- The company does not own the listed properties; instead, it earns revenue by taking a commission from each transaction.

## Objective:
The goal is to analyze Airbnb data to uncover insights into pricing trends, geographical distribution of listings, host performance, and customer reviews. By examining key metrics such as price by room type, availability, and review rates, we aim to understand patterns that can help optimize host revenue, enhance guest experience, and improve overall business performance on the platform.

## Business Risks / Stakeholder Viewpoints

Airbnb faces several challenges in optimizing listing prices, maintaining high review rates, and understanding geographical preferences to attract more guests. Specifically:

>- **1. Pricing Optimization:** What are the trends and variations in pricing across different room types and neighborhoods, and how can hosts optimize their pricing strategies?

>- **2. Host Performance:** Are verified hosts receiving better reviews, and how does this influence booking behavior?

>- **3. Geographical Insights:** Which neighborhoods have the highest concentration of listings, and how does location impact average prices and booking rates?

>- **4.Review Performance:** How does the availability and number of reviews impact booking behavior and overall performance of listings?


# Airbnb Data Profiling and Analysis

## 1. Importing Libraries

```python
import pandas as pd 
import numpy as np
from pandas_profiling import ProfileReport
```

## 2. Load Your Data
Load the dataset into a Pandas DataFrame:
```
import pandas as pd

# Load the dataset
df = pd.read_csv('Airbnb_Open_Data.csv')

# Warning: Handle mixed types
# To avoid DtypeWarning, specify dtype or set low_memory=False
```

## 3. Generate the Profile Report
Create a profile report using the ProfileReport class:

```
from pandas_profiling import ProfileReport

# Generate profile report
profile = ProfileReport(df, title="Airbnb Profiling Report", explorative=True)

# Save report to HTML file
profile.to_file("your_report.html")
```


# Data Cleaning Steps
**1. Remove Duplicates**
Eliminate any duplicate rows from the dataset to ensure data integrity.

**2. Rename Columns**
Standardize column names for consistency and clarity, making them more readable.

**3. Handle Missing Values**
Identify and decide how to address missing values—either by filling them in or removing affected rows.

**4. Standardize Data Types**
Ensure that each column has the correct data type for accurate analysis.

**5. Remove Unnecessary Columns**
Drop any columns that do not contribute to your analysis to streamline the dataset.

**6. Correct Data Formatting**
Standardize text entries and format dates appropriately for analysis.

**7. Outlier Detection** 
Identify and handle outliers to maintain the quality of the data analysis.


# Airbnb Data Analysis Dashboard 🏠
## Project Overview
A comprehensive dashboard analyzing Airbnb listing trends and customer satisfaction metrics from 2003 to 2018, showcasing room type distribution, host patterns, and review performance.

### 📊 Key Metrics

>- **Total Hosts:** 84.4K
>- **Average Price:** $626.3
>- **Total Listings:** 84.4K
>- **Average Review Score:** 32.3



📈 Listing Distribution Analysis
Room Type Breakdown (2003-2018)

Entire homes/apartments: 44,680 listings (53.0%)
Private rooms: 37,947 listings (45.0%)
Shared rooms: 1,662 listings (2.0%)
Hotel rooms: 112 listings (0.1%)

Year-Over-Year Growth

2003: 4,214 total listings
2010: 4,225 listings (stable growth)
2015: 4,280 listings (moderate increase)
2018: 4,206 listings (slight decline)

⭐ Review Performance
Average Reviews by Room Type

Hotel Rooms: 86.09 (Highest rated)

Consistently maintaining premium service quality
Despite low inventory, highest customer satisfaction


Private Rooms: 32.88

Second-best reviewed category
Balanced price-to-satisfaction ratio


Entire Homes/Apartments: 31.80

Stable review performance
Large inventory maintaining consistent quality


Shared Rooms: 26.60

Lower review scores but viable market segment
Opportunity for improvement



📊 Yearly Trends Analysis
Listing Pattern Insights

Entire Homes/Apartments:

Consistent leader in inventory
Average yearly count: ~2,200-2,300 units
Peak in 2014 with 2,326 listings


Private Rooms:

Strong second position
Stable range of 1,850-1,980 listings
Peak in 2018 with 1,959 listings


Hotel Rooms:

Limited but growing presence
Range: 3-9 listings per year
Peak in 2007 with 9 listings


Shared Rooms:

Fluctuating inventory
Range: 64-110 rooms
Peak in 2018 with 110 listings
