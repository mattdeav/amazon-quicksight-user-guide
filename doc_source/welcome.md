# Welcome to Amazon QuickSight\!<a name="welcome"></a>

Amazon QuickSight is a fast business analytics service you can use to build visualizations, perform ad hoc analysis, and quickly get business insights from your data\. Amazon QuickSight discovers AWS data sources, enables organizations to scale to hundreds of thousands of users, and delivers responsive performance by using a robust in\-memory engine \(SPICE\)\.

With Amazon QuickSight, you can do the following:

+ **Get started quickly** – Just sign in, choose a data source, and create your first visualization in minutes\.

+ **Access data from multiple sources ** – Upload files or connect to AWS data sources or external databases\.

+ **Take advantage of optimized visualizations ** – Smart visualizations are dynamically optimized based on the data that you select\.

+ **Get answers fast ** – Generate fast, interactive visualizations on large datasets\.

+ **Tell a story with your data** – Share insights and collaborate with others\.

Amazon QuickSight offers Standard and Enterprise editions\. Both editions offer all of the preceding benefits, while Enterprise edition additionally offers encryption at rest and integration with Microsoft AD directories in AWS Directory Service\. For more information about Amazon QuickSight editions, see [Editions](editions.md)\. For more information about Amazon QuickSight edition pricing, see [Amazon QuickSight](https://quicksight.aws)\.

You use your own data sources to create Amazon QuickSight data sets, which you then use to create [Analyses](#analyses) and visualize your data\. You can also explore Amazon QuickSight using the sample data sets we provide, which are available in your account\. These are also available for download at the following links: 

+ [Business overview](http://quicksightsampledata.s3.amazonaws.com/RevenueData_QuickSightSample.csv)

+ [People overview](http://quicksightsampledata.s3.amazonaws.com/HRData_QuickSightSample.csv)

+ [Sales pipeline](http://quicksightsampledata.s3.amazonaws.com/SalesPipeline_QuickSightSample.csv)

+ [Web and marketing analytics](http://quicksightsampledata.s3.amazonaws.com/MarketingData_QuickSightSample.csv)

There are also a variety of data sets available online, for example:

+ [AWS Public Datasets](https://aws.amazon.com/public-datasets/)

+ [18 places to find data sets for data science projects](https://www.dataquest.io/blog/free-datasets-for-projects/)

+ [Search for "BI Sample Data"](https://www.google.com/search?safe=active&q=bi+sample+data&oq=bi+sample+data)

+ [Search for "Sample Data for Visualization"](https://www.google.com/search?safe=active&q=sample+data+for+visualization)

+ [Search for "Free Sample Databases"](https://www.google.com/search?safe=active&q=free+sample+databases)

These come in a variety of formats\. Some may require that you import the data into a database engine before you can access them\.

To learn more about the major components and processes of Amazon QuickSight, and also the typical workflow for creating data visualizations, use the following sections:


+ [Data](#data)
+ [Analyses](#analyses)
+ [Dashboards](#dashboards)
+ [Typical Amazon QuickSight Workflow](#workflow)
+ [Next Steps](#next-steps-welcome)

## Data<a name="data"></a>

You can use a variety of sources to provide data to Amazon QuickSight, including AWS services, on\-premise databases, and files in several formats\. To learn more about what data sources you can work with in Amazon QuickSight, see [Supported Data Sources](supported-data-sources.md)\.

To work with data, you create *data sets* based on these data sources\. A data set identifies the specific data in a data source that you want to use, for example the table you want to use if you are connecting to a database data source\. A data set also stores any data preparation you have performed on that data \(like renaming a field or changing its data type\), so you don't have to re\-prepare the data each time you want to create an analysis based on it\.

After you have created a data set from a data source, you can create an analysis based on it, as shown in the following illustration:

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/data-flow.png)

You can create multiple analyses using the same data set\. You can also use multiple data sets in a single analysis\.

To learn more about creating data sets, see [Creating Data Sets](creating-data-sets.md)\.

### Data Preparation<a name="data-preparation"></a>

Data preparation is the process of cleaning or transforming raw data from a data source for use in Amazon QuickSight\. This includes things like adding calculated fields, changing field names or data types, or creating SQL queries to refine data\.

To learn more about data preparation, see [Preparing Data](preparing-data.md)\.

### SPICE<a name="spice"></a>

*SPICE* is Amazon QuickSight's *Super\-fast, Parallel, In\-memory Calculation Engine*\. SPICE is engineered from the ground up to rapidly perform advanced calculations and serve data\. Importing your data into SPICE speeds your analytical queries by allowing you to take advantage of its storage and processing capacity\. It also allows you to avoid taking time to retrieve data from a data source whenever you make a change to an analysis or update a visual\.

Each Amazon QuickSight account receives 10 GB of SPICE capacity per paid user, which is allocated when the user signs into Amazon QuickSight for the first time\. Each Amazon QuickSight account also receives one free user with 1 GB of SPICE capacity\.

To learn more about using SPICE, see [Managing SPICE Capacity](managing-spice-capacity.md)\.

## Analyses<a name="analyses"></a>

An *analysis* is the baseline unit for creating and interacting with *visuals*, graphical representations of your data\. Each analysis contains one or more visuals that you assemble for any purpose you choose, such as a sales analysis, cost analysis, or tracking a key performance indicator\. Each analysis also contains a *story*, which you can use to save different iterations of the analysis\.

To learn more about Amazon QuickSight analyses, see [Working with Analyses](working-with-analyses.md)\.

### Visuals<a name="visuals"></a>

A *visual* is a graphical representation of a data set using one of many available visual types\. Amazon QuickSight supports a growing list of visual types including combo charts, heat and tree maps, pivot tables, and others\. 

After you have created a visual, you can modify it in a range of ways, for example by resizing it, or by applying a filter\.

To learn more about Amazon QuickSight visuals, see [Working with Amazon QuickSight Visuals](working-with-visuals.md)\.

### Stories<a name="stories"></a>

A *story* is a set of one or more *scenes* that you can play to step through different iterations of an analysis\. A scene is a representation of an analysis at a given point in time\. It shows the visuals that are on the analysis at that time, but the data in those visuals will continue to update\. It is not a static snapshot\. You *capture* a scene for use in a story\.

To learn more about Amazon QuickSight stories, see [Working with Stories](working-with-stories.md)\.

## Dashboards<a name="dashboards"></a>

A *dashboard* is a read\-only snapshot of an analysis that you can share with other Amazon QuickSight users for reporting purposes\. When you create and publish a dashboard, you specify which users have access to it\. These users can view and filter the dashboard visuals without changing the underlying data\.

To learn more about Amazon QuickSight dashboards, see [Working with Dashboards](working-with-dashboards.md)\.

## Typical Amazon QuickSight Workflow<a name="workflow"></a>

When you create an analysis, the typical workflow is as follows:

1. Connect to a data source, and then create a new data set or choose an existing data set\.

1. \(Optional\) If you created a new data set, prepare the data \(for example, by changing field names or data types\)\.

1. Create a new analysis\.

1. Add a visual to the analysis by choosing fields to visualize\. You can either choose a specific visual type, or use AutoGraph and let Amazon QuickSight choose the most appropriate visual type, based on the number and data types of the fields you select\.

1. \(Optional\) Modify the visual to meet your requirements \(for example, by adding a filter or changing the visual type\)\.

1. \(Optional\) Add more visuals to the analysis\.

1. \(Optional\) Add scenes to the default story to provide a narrative about some aspect of the analysis data\.

1. \(Optional\) Publish the analysis as a dashboard to share insights with other users\.

The following graphic illustrates a typical Amazon QuickSight workflow\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/workflow.png)

## Next Steps<a name="next-steps-welcome"></a>

If you are a new to Amazon QuickSight, see [Signing Up for Amazon QuickSight](signing-up.md) to learn more about creating an Amazon QuickSight account\.