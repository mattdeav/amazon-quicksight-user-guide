# Sorting Visual Data in Amazon QuickSight<a name="sorting-visual-data"></a>

Most visual types offer the ability to change data sort order\. Whether sorting is supported and what visual element you can sort by depends on the visual type\. 

**Important**  
Sorting by text fields \(those with a string data type\) isn't supported for visuals based on SPICE data sets\.

Use the following table to identify the field wells/on\-visual editors that support sorting for each visual type\.


****  

| Visual type | Field well or on\-visual editor | 
| --- | --- | 
| Horizontal bar charts \(all\) | Y axis and Value | 
| Vertical bar charts \(all\) | X axis and Value | 
| Combo charts \(all\) | X axis, Bars, and Lines | 
| Line charts \(all\) | X axis and Value | 
| Pivot table | Column | 
| Scatter plot | Sorting not supported | 
| Tree map | Size, Group by, and Color | 
| Pie graph | Value and Group/Color | 
| Heat map | Columns and Values | 

## Sorting a Visual<a name="sort-a-visual"></a>

For most visual types, you can use either a field well or an on\-visual editor to choose the sort order\. Pivot tables behave differently; you specify the sort order by using the column sort icon on the visual\. For more information about sorting pivot tables, see [Sorting Pivot Tables](sorting-pivot-tables.md)\.

Use the procedures below to sort any non\-pivot table visual type by using either a field well or an on\-visual editor\.

### Sorting by Using an On\-Visual Editor<a name="sorting-element-control"></a>

1. On the visual, choose an on\-visual editor that supports sorting\.

1. On the on\-visual editor menu, choose **Sort**, and then choose the ascending or descending sort order icon\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/bar-sort.png)

### Sorting by Using a Field Well<a name="sorting-field-well"></a>

1. Expand the **Field wells** pane by choosing the expand icon\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/expand-field-wells.png)

1. Choose a field well that supports sorting\. 

1. On the field well menu, choose **Sort**, and then choose the ascending or descending sort order icon\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/sort-field-wells-map.png)