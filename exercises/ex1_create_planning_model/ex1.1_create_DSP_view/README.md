# Create base view for planning model in SAP Datasphere
In this exercise, you will build a view from which we will later create a planning model in SAP Analytics Cloud. In this planning model, we want to plan net working capital by company code. 
<br>You will use a view which was shared from another space and which was derived from a data product in the context of working capital insights. 

1. Go to the databuilder in [SAP Datasphere](https://trial-bdc-datasphere-3.eu10.hcs.cloud.sap/dwaas-core/index.html)
![](images/Ex1.1_1.png)

2. Choose your space

3. Create graphical view

4. Pull the shared view "Net Working Capital Time Series Currency Role (HL)" on to the canvas

5. Add a filter on the year 2024 and enter the following expression: 
   <br>```TimeSeriesYearMonth >=202401```

6. Add a projection and remove all columns except
   - YearMonth
   - Net Working Capital
   - Company Code
  The easiest way to achieve this, is to first select all columns, exclude all columns and afterwards restore the three needed columns. 

7. Set the right view properties
   Business name: NWC_Planning
   Technical name: NWC_Planning
   Exposed for consumption: ON

8. Deploy the view. This saves and deploys the view in your space. 
