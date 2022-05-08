https://www.benlcollins.com/spreadsheets/funnel-charts/

# Funnel charts in Google Sheets using the chart tool, formulas and Apps Script

For all of these examples, we’ll use this fictitious real-estate dataset:

<img src="https://www.benlcollins.com/wp-content/uploads/2016/12/data.jpg" width="450" height="306">

## Funnel charts in Google Sheet with the embedded chart builder

### Step 1: Create a helper column

Move the data from column B into column C, so B1:B7 are now sitting in cell range C1:C7. 
In the new blank column, add the heading “Helper column” and insert the following formula:

```
=(max($C$2:$C$7)-C2)/2
```

This formula determines the max value in our data (in this case 636), 
calculates the difference between the max and the current value and then divides the result by 2 to center the bar, like so:

<img src="https://www.benlcollins.com/wp-content/uploads/2016/12/data_helper.jpg" width="450" height="306">

### Step 2: Insert a chart

Highlight the new data range, including the helper column, and click Insert > Chart....

Make sure you select Stacked Bar Chart from the Chart Types options.

You should end up with a chart like this (image shows how the data is plotted):

<img src="https://www.benlcollins.com/wp-content/uploads/2016/12/helper_cols_chart2.jpg" width="450" height="306">

### Step 3: Set the helper column bar color to none

Set the helper column bars to be transparent, 
thereby “hiding” them to give the appearance of floating bars in a funnel chart.

<img src="https://www.benlcollins.com/wp-content/uploads/2016/12/helper_col_transparent.jpg" width="450" height="306">

### Step 4: Add data labels and remove x-axis

This is an important step. 
Take a look at the x-axis as it stands. 
It’s meaningless really, because our bars are floating in the middle of the chart area.

We can fix this by adding data labels, then removing the x-axis labels altogether:

<img src="https://www.benlcollins.com/wp-content/uploads/2016/12/hide_xaxis.jpg" width="450" height="306">

That’s it!

Our final chart should look something like this:

<img src="https://www.benlcollins.com/wp-content/uploads/2016/11/funnel_chart_1.jpg" width="450" height="306">

## Funnel charts in Google Sheets with sparklines

We can use the sparkline formula to create funnel charts in Google Sheets:

<img src="https://www.benlcollins.com/wp-content/uploads/2016/12/sparkline_chart2.jpg" width="450" height="306">

Assuming we have the same data above, in the range A2:B7, then use the following sparkline formulas:

In column D:
```
=sparkline(B2,
{"charttype","bar";"max",max($B$2:$B$7);
"rtl",true;"color1","#FFA500"})
```

Notice the option "rtl",true, which specifies the direction of the bar within the cell, allowing the symmetrical appearance.

In column E:
```
=sparkline(B2,
{"charttype","bar";"max",max($B$2:$B$7);
"color1","#FFA500"})
```

as follows:

<img src="https://www.benlcollins.com/wp-content/uploads/2016/12/sparkline_chart3.jpg" width="450" height="306">

## Funnel charts in Google Sheets with the REPT function

Another method, similar to the sparkline approach. We use the REPT function and some funky font formatting to create the funnel chart.

Here’s what the final chart looks like:

<img src="https://www.benlcollins.com/wp-content/uploads/2016/12/rept_chart1.jpg" width="450" height="306">

Again, with the data in range A1:B7, add the following formulas into column D:

```
=rept("|",B2/10)
```

The “|” is the pipe symbol, usually found above the Enter key.

The value 10 is a scale factor to ensure the largest bar fits into the cell, 
so feel free to adjust this as needed until your largest bar fits. 
It’s imperative to use the same scale factor value in each formula though.

Next change the font to make the pipe symbols thicker – 
I’ve found font Modak works pretty well for this – 
and then ensure all the cells with the REPT formulas are center aligned. :

<img src="https://www.benlcollins.com/wp-content/uploads/2016/12/rept_chart3.jpg" width="450" height="306">

