# Adding a Filter<a name="adding-a-filter"></a>

You can use filters to refine the data in a data set\. Each filter applies only to a single field\. You can apply filters to both regular and calculated fields\. 

You can apply multiple filters to a single field\. Amazon QuickSight applies the union of all the filters you specify to the field\. 

For example, if there is one filter of `state = WA` and another filter of `sales >= 500`, then the data set only contains records that meet both of those criteria\.

If you create a filter on the `sales` field with the criteria `sales < 400` and another filter with the criteria `sales >= 200`, then the data set contains records with sales amounts between $200 and $399\.99\. 

Take care that multiple filters applied to the same field aren't mutually exclusive\. For example, if you create a filter on the `sales` field with the criteria `sales < 400` and another filter with the criteria `sales > 500`, the data set contains no data\. This result is because the sales amount can't be less than $400 and greater than $500 at the same time\.

**Note**  
The data preview shows you the results of your combined filters, only as they apply to the first 1000 rows\. If all of the first 1000 rows are filtered out, then no rows show in the preview\. This result happens even when rows after the first 1000 aren't filtered out\.


+ [Viewing Filters](viewing-filters-data-prep.md)
+ [Adding a Filter](add-a-filter-data-prep.md)
+ [Editing a Filter](edit-a-filter-data-prep.md)
+ [Deleting a Filter](delete-a-filter-data-prep.md)