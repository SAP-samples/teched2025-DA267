# Create the seamless planning model in SAP Analytics Cloud
In this exercise, we will use the NWC_PLANNING view from SAP Datasphere and use it to build a seamless planning model. 

> [!NOTE]  
> We will use the new live version feature that is delivered in QRC4 2025. Find more information [here](https://community.sap.com/t5/technology-blog-posts-by-sap/unlocking-the-next-chapter-of-seamless-planning-in-sap-business-data-cloud/ba-p/14243864)

1. Go to the modeler in [SAP Analytics Cloud](https://trial-bdc-sac-3.eu10.sapanalytics.cloud/sap/fpa/ui/app.html#/home)
![](https://github.com/SAP-samples/teched2025-DA267/blob/04340a99e350ed2729b04867a0f2c2f3eade5cd6/images/ex1.2_1.png)

2. Create new model
![](https://github.com/SAP-samples/teched2025-DA267/blob/04340a99e350ed2729b04867a0f2c2f3eade5cd6/images/ex1.2_2.png)

3. Select SAP Datasphere and your user's space as data storage location. Selecting SAP Datasphere as data storage location means that you will use seamless planning.
![](https://github.com/SAP-samples/teched2025-DA267/blob/04340a99e350ed2729b04867a0f2c2f3eade5cd6/images/ex1.2_3.png)

4. Now you select the datasource for your model. We select SAP Datasphere. By that, we will directly create a live connection to our source view via a live version.
![](https://github.com/SAP-samples/teched2025-DA267/blob/04340a99e350ed2729b04867a0f2c2f3eade5cd6/images/ex1.2_4.png)

5. Select the view that you created in [exercise 1.1](../../../exercises/ex1_create_planning_model/ex1.1_create_DSP_view/README.md)
![](../../../images/ex1.2_5.png)

6. Now the planning model is created. Let's find out the live version is highlighted (no action needed). We see the live version in the data preview and it is listed under External Live Version Data Sources. We do not have to perform mappings now. We will learn how to do so later. 
![](../../../images/ex1.2_28.png)

7. We now have to define semantics for our model columns and add master data wherever required. First, make the TimeSeriesYearMonth column the model's Date dimension.
![](../../../images/ex1.2_6.png)

8. The system identified the right settings already. Confirm with OK.
![](../../../images/ex1.2_7.png)

9. Save the model. Save it under My Files and give it a name. E.g., TECHED2025_DA267_USERxx.
![](../../../images/ex1.2_8.png)
![](../../../images/ex1.2_9.png)

10. Create a (public) dimension table for Company Code. 
> [!CAUTION]
> Give it a user-specific name and make it a public dimension. Otherwise, you will not be able to proceed with the next step. Where we load master data.

![](../../../images/ex1.2_10.png)
![](../../../images/ex1.2_11.png)

11. Open the dimension table to edit it. 
![](../../../images/ex1.2_12.png)

12. Add a parent-child hierarchy. You can give it any name. 
![](../../../images/ex1.2_13.png)
![](../../../images/ex1.2_14.png)

13. Save.
![](../../../images/ex1.2_15.png)


> [!NOTE]  
> We need to load master data via OData - even with seamless planning. In the future, we want to provide replication-free access to master data as well. 


15. Navigate to Data Management via the drop-down in the top left coner. Then import data from datasource.
![](../../../images/ex1.2_16.png)

16. Select OData
