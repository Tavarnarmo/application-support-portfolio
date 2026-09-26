# Monthly report generation failed

## Problem

The user tried to generate the monthly sales report for August. After loading, the application showed the error message: Report generation failed. Error code: RPT-504.

## Diagnostics

According to the procedure, I checked the possible causes of RPT-504. The reporting service was running normally, and there were no other similar tickets.
I checked the logs and found the following messages:
WARN Query execution exceeded 30s
ERROR Report generation timeout
I also noticed that the number of records was significantly higher than in the previous month.
I had a hypothesis that the Report generation timeout error might be caused by processing a large amount of data. To test this, I tried to generate the report with a smaller 
number of records. The report was generated successfully.
The user needed the report for the full month, so generating it with a smaller number of records was not a sufficient workaround. I therefore escalated the case to L2 support.

## Root cause

L2 found that some of the sales records for August had been duplicated after an import from an external system, which caused SALES_MONTHLY to process more data than it should have.

## Resolution

L2 removed the duplicated records and recalculated the report data. I then asked the user to generate the monthly report again.


