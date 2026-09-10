# airbnb_data-analysis


📌 Project Overview

This project performs Exploratory Data Analysis (EDA) on the Airbnb Open Data dataset. The main goal is to understand Airbnb listings based on their location, room type, pricing, reviews, availability, and host-related information.

The project starts with data loading and quality checking, followed by cleaning missing values, removing duplicates, correcting inconsistent borough names, validating numerical values, and creating visualizations.

The analysis is designed as a beginner-friendly Data Analytics / EDA project using Python.

🎯 Objectives

Load and inspect the Airbnb dataset.

Understand the structure, columns, and data types.

Identify and handle duplicate records.

Analyze missing values.

Clean categorical and numerical data.

Correct inconsistent neighbourhood group names.

Validate minimum nights and availability values.

Analyze listings by borough and room type.

Compare Airbnb prices across room types and neighbourhood groups.

Examine the relationship between price and number of reviews.

Create charts for easy interpretation.

📂 Dataset

Dataset: Airbnb Open Data

The dataset contains Airbnb listing information such as:

Listing ID

Host ID

Host name

Neighbourhood group

Neighbourhood

Latitude and longitude

Room type

Construction year

Price

Service fee

Minimum nights

Number of reviews

Reviews per month

Review rating

Host listing count

Availability

House rules

License

The original dataset contains 102,599 rows and 26 columns before duplicate removal and further cleaning.

🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook / Google Colab

🔄 Project Workflow

Dataset
   ↓
Load Data
   ↓
Initial Inspection
   ↓
Check Shape & Columns
   ↓
Check Data Types
   ↓
Statistical Summary
   ↓
Duplicate Detection & Removal
   ↓
Missing Value Analysis
   ↓
Data Cleaning
   ↓
Data Validation
   ↓
Exploratory Data Analysis
   ↓
Data Visualization
   ↓
Insights

🧹 Data Cleaning Performed

1. Duplicate Removal

Duplicate rows were identified and removed.

Duplicate rows found: 541

Duplicate rows remaining after removal: 0

2. Missing Categorical Values

Missing categorical values were replaced with Unknown for columns such as:

NAME

host_identity_verified

host name

neighbourhood group

neighbourhood

country

country code

cancellation_policy

house_rules

3. Review Data

Missing review counts and reviews-per-month values were treated as zero.

4. Missing Price

Rows with missing price values were removed because price is an important variable for the analysis.

5. Inconsistent Borough Names

Some spelling variations were corrected:

manhatan → Manhattan

brookln → Brooklyn

6. Numerical Validation

Values outside reasonable ranges were treated as missing:

Minimum nights: 1–365

Availability: 0–365

Median values were then used for imputation.

7. Other Numerical Missing Values

Median imputation was applied to selected numerical columns such as:

Construction year

Service fee

Calculated host listings count

8. Location Data

Rows with missing latitude or longitude were removed.

9. License Column

The license column was removed because it contained only 2 non-null values, making it unsuitable for this beginner-level analysis.

📊 Analysis Performed

1. Listings by Borough

Counts the number of Airbnb listings in each neighbourhood group.

2. Listings by Room Type

Shows how listings are distributed among different room types.

3. Average and Median Price

The cleaned dataset produced approximately:

Average price: $625.36

Median price: $625.00

4. Price Distribution by Room Type

A box plot is used to compare price distributions across room types.

5. Price Distribution by Neighbourhood Group

A box plot compares Airbnb prices between neighbourhood groups.

6. Price vs Number of Reviews

A scatter plot is used to examine whether listing price appears to be related to the number of reviews.

📈 Visualizations

The notebook includes:

Airbnb Listings by Borough

Airbnb Listings by Room Type

Price Distribution by Room Type

Price Distribution by Neighbourhood Group

Price vs Number of Reviews

Combined Airbnb Data Dashboard

💡 Key Questions

This project helps answer questions such as:

Which borough has the most Airbnb listings?

Which room type is most common?

What is the average Airbnb price?

How does price vary by room type?

How does price vary by neighbourhood group?

Is there an apparent relationship between price and number of reviews?

What data quality issues exist in the dataset?

🚀 How to Run

Google Colab

Open the .ipynb file in Google Colab.

Upload Airbnb_Open_Data.xlsx.

Make sure the Excel file is available at:

/content/Airbnb_Open_Data.xlsx

Run the notebook cells from top to bottom.

Local Jupyter Notebook

Install the required libraries:

pip install pandas numpy matplotlib seaborn openpyxl jupyter

Then place Airbnb_Open_Data.xlsx in the same folder as the notebook and update the file path if required.

📁 Project Structure

Airbnb-Data-Analysis/
│
├── Airbnb_Open_Data.xlsx
├── Airbnb_Data_Analysis.ipynb
└── README.md

🔮 Future Improvements

The project can be extended by adding:

Interactive Streamlit dashboard

Price outlier analysis

Correlation heatmap

Top expensive and affordable neighbourhoods

Availability analysis

Review rating analysis

Host activity analysis

Geographic/map-based visualization

More advanced statistical analysis

Machine learning for price prediction
