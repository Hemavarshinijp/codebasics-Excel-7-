# codebasics-Excel-7-

In this dataset i used power query to clean, merge , added queries 

## Cleaning data
Removing duplicates
Replace null to Not Available
TRIM to speace space
Split the column by delimeter
# key notes
Power Query simplifies data cleaning and transformation compared to using Excel formulas.
Power Query uses M-language internally for all the steps performed using the UI controls.
It is advisable to give meaningful names to the transformation steps in Power Query. (Your future self will thank you for this!)

## Merging data
Merging two tables in power query
# key notes
In Power Query, you can perform various types of joins between tables based on your specific requirements.
Take some time to explore all the options in Power Query and familiarize yourself with them.
To quickly check the quality status of columns, use the "view" option.
Unique values are values that appear only once in the data.
Distinct values are values that appear at least once in the data

## Adding new column
Added conditional columns and custom column 
# conditional column
if unit = Billion then 1000 else 1 as unit_factor
# custom column
Budget mil = budget * unit_factor
Revenue mil = Revenue * unit_factor
Budget INR = if [currency] ="USD" then [Budget mil] *80 else [Budget mil]
Revenue INR = if [currency] ="USD" then [Revenue mil] *80 else [Revenue mil]
Budget USD = if [currency] ="INR" then [Budget mil] /80 else [Budget mil]
Revenue USD = if [currency] ="INR" then [Revenue mil] /80 else [Revenue mil]
# key notes
Power Query simplifies data cleaning and transformation compared to using Excel formulas.
Power Query uses M-language internally for all the steps performed using the UI controls.
It is advisable to give meaningful names to the transformation steps in Power Query. (Your future self will thank you for this!)
