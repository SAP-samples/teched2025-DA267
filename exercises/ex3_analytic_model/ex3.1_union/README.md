# Bring plan and actual data together in SAP Datasphere in a union view
In this exercise, we will first build a union to combine plan and actual data. Then, we will build an analytic model on top of it [exercise 3.2](../ex3.2_analytic_model). 

> [!NOTE]  
> You may wonder why we again create a plan vs. actual comparison as we could also report on the planning model directly which also has the plan data and live actuals. There are many reasons why you will need an analytic model in real life. In this exercise, we simplified heavily. 
> - Use time-dependet master data, hierarchies, texts etc. (this what we do in this exercise)
> - Use the full granularity of actuals that you may not want to have in your planning model (performance!). Imagine loading the full ACDOCA table to a planning model... Does not sound right!
> - Use attributes etc. that are not part of your planning model
> - Data may be homogenous. SAP Datasphere will give you everything you need to align models
> - Share plan data in many analytic scenarios and across domains.

1. Go back to [SAP Datasphere](https://trial-bdc-datasphere-3.eu10.hcs.cloud.sap/dwaas-core/index.html), go to the data builder, select your space and create a new graphical view.

2. 
