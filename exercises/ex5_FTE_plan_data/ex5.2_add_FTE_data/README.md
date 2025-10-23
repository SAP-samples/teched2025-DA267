# Add a live version for FTE data to the planning model
We now want to add data from an HR planning model with FTE (full-time equivalent) data to our planning model. HR planning does not happen on the same dimensionality so we have to add information to it.

1. Go back to [SAP Datasphere](https://trial-bdc-datasphere-3.eu10.hcs.cloud.sap/dwaas-core/index.html), go to the data builder, select your space and create a new graphical view.
2. In the graphical view, add the shared table *FTE_PLANNING_FACTS*. This is the exposed fact table of the HR planning model.
3. Pull the shared table *Org Unit Master* on *FTE_PLANNING_FACTS* and create a join.
![](../../../images/ex5.2_1.png)

4. 
