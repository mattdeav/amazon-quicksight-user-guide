# Filtering Visual Data in Amazon QuickSight<a name="filtering-visual-data"></a>

You can use filters to refine the data displayed in a visual\. Filters are applied to the data before any aggregate functions that you specify\.

A filter is associated with a single data set in an analysis, and can be scoped to one, several, or all visuals in the analysis that use that data set\. By default, a filter applies to the visual that was selected when the filter was created\. You can change the scope of a filter after you create it\.

You can apply filters to both regular fields and calculated fields\. 

You can apply multiple filters to a single field\. Amazon QuickSight applies the union of all the filters you specify to the field\. For example, if you create a filter on the `sales` field with the criteria `sales < 400` and another filter with the criteria `sales >= 200`, then the visual shows records with sales amounts between $200 and $399\.99\. You must make sure that multiple filters applied to the same field aren't mutually exclusive\. For example, suppose that you create a filter on the `sales` field with the criteria `sales < 400` and another filter with the criteria `sales > 500`\. In this case, the visual shows no data, because the sales amount can't be both less than $400 and greater than $500 at the same time\.

You can apply multiple filters to a visual\. Amazon QuickSight applies the union of all the filters you specify to the visual\. For example, if there is one filter of `state = WA` and another filter of `sales >= 500`, then the visual only displays records that meet both of those criteria\.

Amazon QuickSight uses filters to focus on or exclude a visual element representing a particular value\. For more information about focusing on a visual element, see [Focusing on Visual Elements](focusing-on-visual-elements.md)\. For more information about excluding a visual element, see [Excluding Visual Elements](excluding-visual-elements.md)\.


+ [Viewing Filters](viewing-filters.md)
+ [Adding a Filter](add-a-filter.md)
+ [Editing a Filter](edit-a-filter.md)
+ [Deleting a Filter](delete-a-filter.md)