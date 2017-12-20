# Quick Start: Create an Analysis with a Single Visual Using Sample Data<a name="quickstart-createanalysis"></a>

Use the following procedure to use the Web and Social Media Analytics sample data set to create an analysis containing a line chart visual\. This visual shows the count by month of people that have added themselves to the mailing list\. If you don't see the Web and Social Media Analytics sample data already in Amazon QuickSight, you can download it from [http://quicksightsampledata\.s3\.amazonaws\.com/MarketingData\_QuickSightSample\.csv](http://quicksightsampledata.s3.amazonaws.com/MarketingData_QuickSightSample.csv)\.

1. On the Amazon QuickSight start page, choose **New analysis**\.

1. On the **Your data sets** page, choose the **Web and Social Media Analytics** data set and then choose **Create Analysis**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/quickstart-analysis.png)

1. In the **Fields list** pane, choose **Date** and then choose **Mailing list adds**\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/quickstart-fields.png)

   Amazon QuickSight uses AutoGraph to create the visual, selecting the visual type it determines is most compatible with those fields\. In this case, it is a line chart that shows mailing list adds by year, which is the date granularity default\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/quickstart-visual.png)

1. Expand the **Field wells** pane by choosing the expand icon\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/quickstart-expand.png)

1. Choose the **X axis** field well, choose **Aggregate**, and then choose **Month**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/quickstart-date.png)

   The line chart updates to show mailing list adds by month, rather than by the default of by year\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/quickstart-visual2.png)