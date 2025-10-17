# Create base view for planning model in SAP Datasphere
In this exercise, you will build a view from which we will later create a planning model in SAP Analytics Cloud. In this planning model, we want to plan net working capital by company code. 
<br>You will use a view which was shared from another space and which was derived from a data product in the context of working capital insights. 

1. Create graphical view

2. Pull the shared view "Net Working Capital Time Series Currency Role (HL)" on to the canvas

3. Add a filter on the year 2024 and enter the following expression: 
   <br>```TimeSeriesYearMonth >=202401```

4. Add a projection and remove all columns except
   - YearMonth
   - Net Working Capital
   - Company Code
  The easiest way to achieve this, is to first select all columns, exclude all columns and afterwards restore the three needed columns. 

5. Set the right view properties
   Business name: NWC_Planning
   Technical name: NWC_Planning
   Exposed for consumption: ON

6. Deploy the view. This saves and deploys the view in your space. 
