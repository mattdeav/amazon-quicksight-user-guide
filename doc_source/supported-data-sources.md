# Supported Data Sources<a name="supported-data-sources"></a>

Amazon QuickSight supports a variety of data sources that you can use to provide data for analyses\. The following data sources are supported:

## Relational Data Sources<a name="relational-data-sources"></a>

You can use any of the following relational data stores as data sources for Amazon QuickSight:

+ Amazon Athena

+ Amazon Aurora

+ Amazon Redshift

+ Amazon Redshift Spectrum

+ Amazon S3

+ Amazon S3 Analytics

+ Apache Spark 2\.0 or later

+ MariaDB 10\.0 or later

+ Microsoft SQL Server 2012 or later

+ MySQL 5\.1 or later

+ PostgreSQL 9\.3\.1 or later

+ Presto 0\.167 or later

+ Snowflake

+ Teradata 14\.0 or later

You can retrieve data from tables and materialized views in PostgreSQL instances, and from tables in all other database instances\.

Amazon Redshift clusters, Amazon Athena databases, and Amazon Relational Database Service \(RDS\) instances must be in AWS\. Other database instances must be in one of the following environments to be accessible from Amazon QuickSight:

+ Amazon EC2

+ On your local network

+ In a data center or some other internet\-accessible environment

## File Data Sources<a name="file-data-sources"></a>

You can use files in Amazon S3 or on your local network as data sources for Amazon QuickSight\. Amazon QuickSight supports files in the following formats:

+ Microsoft Excel files \(\.xlsx files\) on your local network\.

+ Delimited\-text files \(for example, \.csv and \.tsv files\) on your local network or in Amazon S3\.

+ Common log format \(\.clf\) and extended log format \(\.elf\) files on your local network or in Amazon S3\.

Files in Amazon S3 that have been compressed with zip, or gzip \([www\.gzip\.org](http://www.gzip.org)\), can be imported as\-is\. If you used another compression program for files in Amazon S3 , or if the files are on your local network, you need to unzip them before importing them\.

## Software as a Service \(SaaS\) Data Sources<a name="service-data-sources"></a>

+ Salesforce

  You can use reports or objects in the following editions of Salesforce as data sources for Amazon QuickSight\. Joined reports aren't supported as Amazon QuickSight data sources\.

  + Enterprise Edition

  + Unlimited Edition

  + Developer Edition