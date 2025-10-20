# Create base view for planning model in SAP Datasphere
In this exercise, you will build a view from which we will later create a planning model in SAP Analytics Cloud. In this planning model, we want to plan net working capital by company code. 
<br>You will use a view which was shared from another space and which was derived from a data product in the context of working capital insights. 

1. Go to the databuilder in [SAP Datasphere](https://trial-bdc-datasphere-3.eu10.hcs.cloud.sap/dwaas-core/index.html)
![](https://github.com/SAP-samples/teched2025-DA267/blob/dfa1c77d51d821227bf0e65ee7b8e9adf514a5d6/images/ex1.1_1.png)

2. Choose your space
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_2.png)

3. Create graphical view
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_3.png)

4. Pull the shared view "Net Working Capital Time Series Currency Role (HL)" on to the canvas
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_4.png)

5. Filter on the year 2024 by adding a filter and entering the following expression: 
   <br>```TimeSeriesYearMonth >=202401```
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_5.png)
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_6.png)

6. Add a projection and remove all columns except
   - YearMonth
   - Net Working Capital
   - Company Code
  The easiest way to achieve this is to first select all columns, exclude all columns and afterwards restore the three needed columns. 
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_7.png)
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_8.png)

7. Set the right view properties and deploy the view. This saves and deploys the view in your space. The warning is not important for our scenario, so click deploy anyway.
   Business name: NWC_Planning
   Technical name: NWC_Planning
   Exposed for consumption: ON
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_9.png)
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_10.png)
![](https://github.com/SAP-samples/teched2025-DA267/blob/ed12e696e4b88e9065af5eb316304ef7685e590c/images/ex1.1_11.png) 
