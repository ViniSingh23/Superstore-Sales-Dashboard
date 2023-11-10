# Superstore Sales Dashboard with Enhanced Data Preprocessing in PowerBI

Welcome to the Superstore Sales Dashboard project! This PowerBI-based dashboard provides a comprehensive view of your sales data, and I've streamlined the data preprocessing steps to make your reporting experience even more efficient.
# NOTE: Ensure PowerBI is installed on your PC.

# Instructions for Data Preprocessing:

1. # Load Data in PowerBI:
   - Import your Excel data into PowerBI.
   - Navigate to the "Table View."

2. # Data Formatting:
   - Change the format of the "ORDER DATE" and "SHIP DATE" columns to "dd/mm/yyyy." (By clicking on the column and then format)

3. # Create New Columns:
   - *MONTH Column:*
     - Rename the column to "Month."
     - Use the formula: Month = Orders[Order Date].[Month]

   - *QUARTER Column:*
     - Create a new column for "Quarter."
     - Write the formula: Quarter = Orders[Order Date].[Quarter]

   - *YEAR Column:*
     - Establish the "Year" column.
     - Write the formula: Year = Orders[Order Date].[Year]

   - *Day of Week Column:*
     - Introduce the "Day of Week" column.
     - Write the formula: Day of Week = WEEKDAY(Orders[Order Date], 2)

   - *WEEKDAY/WEEKEND Column:*
     - Generate a column for "Weekday/Weekend."
     - Write the formula: Weekday/Weekend = IF(Orders[Day of Week]=6 || Orders[Day of Week]=7, "Weekend", "Weekday")

   - *Days for Shipment Column:*
     - Calculate the "Days for Shipment" column.
     - Write the formula: Days for Shipment = DATEDIFF(Orders[Order Date], Orders[Ship Date], DAY)

   - *Full Name Column:*
     - Concatenate the first and last names into a "Full Name" column.
     - Write the formula: Full Name = Orders[First Name] & " " & Orders[Last Name]

4. # Format Columns:
   - Click on the "SALES" column and change the format to "Currency."
   - Adjust the "PROFIT" column decimal point digits from "Auto" to "2."

5. # Proceed to Report View:
   - Click on "Report View" to start creating your comprehensive sales report.

The data is now optimized and ready for insightful reporting. Dive into the Report View to explore and analyze your Superstore sales data effortlessly!
