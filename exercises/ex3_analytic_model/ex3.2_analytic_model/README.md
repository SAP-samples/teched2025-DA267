# Create an analytic model in SAP Datasphere
In this exercise, we use the view created in [exercise 3.1](../ex3.1_union) and build an analytic model and preview the data. 

> [!TIP]
> The Analytic Model is one of the cornerstones of SAP Datasphere. It allows multi-dimensional and semantically rich analytical modelling to answer business questions easier, faster and more efficiently. Want to learn more?
> - [Blogpost - Introducing the Analytic Model in SAP Datasphere](https://community.sap.com/t5/technology-blog-posts-by-sap/introducing-the-analytic-model-in-sap-datasphere/ba-p/13568591)
> - [Analytic Model Documentation in SAP Help Portal](https://help.sap.com/docs/SAP_DATASPHERE/c8a54ee704e94e15926551293243fd1d/e5fbe9e2cb93484dab8b1963145e565f.html)

1. In the first step, we review the analytic model. As you see, measure, dimensions and associations are taken over from the union that was created earlier. The company code dimension is time-dependent as indicated by the clock icon.
![](../../../images/ex3.2_1)

2. Provide a business name and a technical name and save the analytic model. Do not deploy it yet. We'll come back later.
![](../../../images/ex3.2_2)

3. We want to create a reference date variable to filter our time-dependent company code master data. The variable shall have a dynamic default value referring to today's date and should be adjustable for the reporting users. This is why we need to create a lookup entity in the next steps. 
![](../../../images/ex3.2_3)

> [!TIP]
> The Analytic Model offers three ways to fill variables:
> - Manual input
> - Derive Value: Derived variables are hidden in the data preview or in an SAP Analytics Cloud story. See Derived Variables.
> - Dynamic Default: You get a derived value in the parameter dialog list when opening the analytic preview, and in the variable prompt for an SAP Analytics Cloud story. See Dynamic Default.

4. Navigate to the data builder by clicking on the *back* arrow or the space name at the top left. Then create a new SQL view.
![](../../../images/ex3.2_4)
![](../../../images/ex3.2_5)

5. Enter the following SQL and preview your data. Then name your view and deploy it.
![](../../../images/ex3.2_6)

