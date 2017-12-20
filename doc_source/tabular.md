# Using Tabular Reports<a name="tabular"></a>

Use tabular reports to see a customized table view of your data\.

To create a table visual, choose at least one field of any data type\. You can add as many columns as you need\. Plus, you can add calculated columns\. 

The icon for a table is as follows\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/tabular-icon.png)

## Tabular Report Features<a name="tabular-report-features"></a>

Tabular reports don't display a legend\. You can hide or display the title on a tabular report\.

Use the following table to understand the features supported by tabular reports\. 


****  

| Feature | Supported? | For More Information | 
| --- | --- | --- | 
| Changing the legend display | No | [Displaying the Visual Legend](formatting-a-visual.md#displaying-the-visual-legend) | 
| Changing the title display | Yes | [Displaying a Visual's Title](formatting-a-visual.md#displaying-visual-title) | 
| Sorting | Yes | [Sorting Visual Data in Amazon QuickSight](sorting-visual-data.md) | 
| Calculated Fields & Aggregations | Yes | [Changing Field Aggregation](changing-field-aggregation.md) | 
| Adding drill\-downs | No | [Adding Drill\-Downs to Visual Data in Amazon QuickSight](adding-drill-downs.md) | 

## Creating a Tabular Report<a name="create-pivot-table"></a>

Use the following procedure to create a tabular report \(a table visual\)\.

1. On the analysis page, choose **Visualize** on the tool bar\.

1. Choose **Add** on the application bar, and then choose **Add visual**\.

1. On the **Visual types** pane, choose the table icon\.

1. From the **Fields list** pane, choose the fields you want to use\. If you want to add a calculated field, choose **Add** on the application bar, and then choose **Add calculated field**\.

   To create a non\-aggregated view of the data, add fields only to the **Value** field well\. This shows data without any aggregations\.

   To create an aggregated view of the data, choose the fields you want to aggregate by, and then add them to the **Group by** field well\.