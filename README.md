# Data-Analysis-of-Building-Energy-Benchmarking-Data
This analysis explores the City of Calgary’s Building Energy Benchmarking dataset to identify energy consumption trends and efficiency insights for sustainable development.
# How Regex was used for data extraction and cleaning.
Regular Expressions (Regex) were applied in multiple areas to clean and extract meaningful data from the dataset. 
# 1. Extracting Numeric Values from Text-Based Columns
Some numeric columns (e.g., Property GFA, Energy Use, and Emissions) may contain unwanted text or units. To clean these, Regex was used to extract only numeric values.Here \d+ → Matches one or more digits (e.g., 456),\.? → Matches an optional decimal point ,\d* → Matches any digits after the decimal (e.g., .45 in 123.45).
# 2. Standardizing Postal Codes in candian format
Some postal codes might be missing spaces, lowercase letters, extra characters. Regex was used to ensure the proper format.here ([A-Z]\d[A-Z]) used the first three characters of a postal code, \s* is used for Matches zero or more spaces, (\d[A-Z]\d) is used the last three characters of a postal code.
# 3. Cleaning Property Names & Addresses
Property names and addresses might contain extra characters, inconsistent spacing, or unnecessary details. Regex was used to clean them up.r^a-zA-Z0-9\s this Regex is used to remove special characters from a string, keeping only letters (A-Z, a-z), numbers (0-9), and spaces (\s).
# Challanges Faced
Here in this data set is inconsisting formating some numeric columns contained units or extra text so Regex was used to extract only numeric values and convert them to floats.
Some properties had extremely high energy usage compared to others so Used the IQR method to detect outliers and replaced extreme values with the median.
# Insights Gain
Commercial buildings had significantly higher energy consumption than residential ones.
Energy use intensity has declined in recent years, suggesting improved efficiency in some buildings.
The T-test showed a statistically significant difference in energy efficiency between Offices and Residential Buildings, confirming that offices tend to have lower Energy Star Scores.
