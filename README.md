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

