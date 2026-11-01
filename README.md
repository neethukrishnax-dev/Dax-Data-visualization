Calculated Columns
1) Select the Order Details table
   Click on New Column
   Category Type ='Order Details'[Category] & " - " & 'Order Details'[Sub-Category]
2) Select the Order Details table
   Click on NewColumn
   Revenue per Order ='Order Details'[Amount] * 'Order Details'[Quantity]
3)  Select the Order Details table
    Click on New Column
    Sales Category =IF( 'Order Details'[Amount] > AVERAGE('Order Details'[Amount]),  "Above Average",  "Below Average")

Calculated Measures
 1)Select the Order Details table > New Measure > Order Count =DISTINCTCOUNT('Order Details'[Order ID])
 2)Select the Order Details table > New Measure >Average Profit in Delhi =CALCULATE(  AVERAGE('Order Details'[Profit]), 'List of Orders'[City] = "Delhi")
 3)Select the Order Details table > New Measure > YTD Sales =CALCULATE(SUM('Order Details'[Revenue per Order]), DATESYTD('List of Orders'[Order Date])

Data Visualization
 1) Report View > Select the Clustered Column > Drag the Category(x Axis) > Drag the Amount(Y Axis) > Drag the Target(Y Axis) Add a chart title
 2) Select the Donut Chart  > Drag Sub-Category > Drag Profit Margin > Set the chart title
 3) Selected a Line Chart >  Added Order Date (Year and Month)  X-axis > Added Amount to the Y-axis >Set the chart title
 4) Scatter Chart > Quantity to the X-axis >  Profit to the Y-axis > Added Sub-Category to the Details > Set the chart title
 5) Created a Card visual to display the total sales amount using Sum of Amount
      Created another Card visual to display the total sales target using Sum of Target
      Created a Multi-row Card to display Category and Target
      Set the chart title
 6) Matrix  > Category to the Rows  > Month of Order Date to the Columns  > Amount to the Values > Set the chart title
 7) Map > State column from the List of Orders table > Amount column from the Order Details table >  Set the chart title
 8) Selected the Tree map >  Sub-Category > Amount  > Added the title
 9)  Funnel Chart >State from the List of Orders table > Order ID from the Order Details table > Added the title
