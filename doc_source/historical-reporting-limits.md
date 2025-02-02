# Report Limits<a name="historical-reporting-limits"></a>

Historical metrics reports have the following limits:

**Data only for active queues**
+ You can get data only for active queues\. A queue is inactive if there are no contacts in the queue and no agents available\.
+ This applies to the `GetMetricsData` and `GetCurrentMetricsData` API as well\. This means that if a queue is not considered active, if you query for its metrics using the API you won't get any data\.
+ The user interface shows up to 100 queues\. If you have more than 100 active queues, add a filter to scope the report to the queues of interest\.

**UI Displays Up to 100 Queues**
+ The user interface shows up to 100 queues\. If you have more than 100 active queues, add a filter to scope the report to the queues of interest\.

**80k Cell Limit**

There is currently an 80k cell limitation on historical metrics reports and scheduled reports\. This applies to the total number of cells \(columns \* rows\), accounting for grouping and filtering\. 

For example, let's say you create a historical metrics report with this criteria: 
+ Grouped by agents
+ With an interval of 30 minutes
+ For the last 24 hours
+ Limited to include only 5 metrics
+ Filtered to show only contacts handled in BasicQueue

If only 10 agents handled contacts in BasicQueue during this time, then you would expect to see \(24\*2\)\*5\*10 = 2400 cells that count towards the 80k limit\.

If you reach the limit, a message will appear in the UI letting you know\. 