
# Hotel Bookings Data Analysis

This project focuses on cleaning, transforming, and analyzing hotel booking data to understand booking patterns and improve insights for business decisions.

## Dataset

The dataset contains hotel booking records, including:
- Hotel type
- Arrival dates (year, month, day)
- Customer details (agent, customer type, etc.)
- Reservation status and related fields

## Key Steps in the Analysis

### 1. Data Cleaning
- Removed unwanted characters from text columns (e.g., `hotel` column).
- Fixed column name inconsistencies.
- Converted `arrival_date` to proper datetime format.
- Removed duplicates using `.drop_duplicates(keep="first")`.

### 2. Feature Engineering
- Combined `arrival_date_year`, `arrival_date_month`, and `arrival_date_day_of_month` into a new `arrival_date` column.
- Extracted year and month from the `arrival_date` for further analysis.
- Reorganized columns to group related data logically.

### 3. Exploratory Data Analysis
- Identified the unique hotel types.
- Checked for missing and duplicate entries.
- Planned analysis to include booking trends, cancellations, and revenue by customer type and time.

## Common Issues & Fixes

- SettingWithCopyWarning: Resolved by using `.copy()` or `.loc[]` to avoid unintended side effects.
- KeyError / AttributeError: Ensured correct column names and data types before accessing or transforming columns.
- ValueError in drop_duplicates: Corrected the `keep` parameter to lowercase `"first"`.

## Tools Used
- Python
- Pandas
- Jupyter Notebook

## Learnings
- Handling and cleaning real-world datasets.
- Working with datetime objects and extracting features.
- Best practices in avoiding pandas warnings and writing safe DataFrame operations.

## To Run
1. Install required packages:
   ```bash
   pip install pandas jupyter
   ```
2. Open the notebook and run step-by-step.

Feel free to modify and build on this analysis for deeper insights or integration with visualization tools (e.g., Matplotlib, Seaborn).
