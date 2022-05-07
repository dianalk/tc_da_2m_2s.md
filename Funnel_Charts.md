https://www.benlcollins.com/spreadsheets/funnel-charts/

# Funnel charts in Google Sheets using the chart tool, formulas and Apps Script

### Step 1: Create a helper column

Move the data from column B into column C, so B1:B7 are now sitting in cell range C1:C7. 
In the new blank column, add the heading “Helper column” and insert the following formula:

=(max($C$2:$C$7)-C2)/2
