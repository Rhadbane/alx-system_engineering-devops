![Postmortem Image](postmortem.jpg)

0x19-postmortem


Issue Summary

Duration: The outage occurred on August 12, 2024, from 14:00 to 15:30 UTC, lasting 1 hour and 30 minutes.

Impact: The outage affected the "QuickBooks Online" service, causing slow response times and intermittent access issues for users. Approximately 60% of users experienced difficulties accessing their accounts or processing transactions during this period.

Root Cause: The root cause was a database connection pool exhaustion due to a misconfigured query that led to a spike in resource consumption.

Timeline

- 13:55 : Monitoring system detected increased latency in database queries.
-14:00 : OUTAGE BEGINS — Users reported slow response times and intermittent access issues.
- 14:05 : Monitoring alert triggered, notifying the on-call engineer.
- 14:10 : Initial investigation began, focusing on the application server performance.
- 14:20 : Misleading path: Assumed a network issue and checked network configurations.
- 14:30 :Escalated to the database team after ruling out network issues.
- 14:40 : Identified high database connection usage; suspected a query issue.
- 14:50 : Database logs reviewed, revealing a poorly optimized query consuming excessive resources.
- 15:00 : Query optimization initiated by the database team.
- 15:20 : Optimized query deployed, reducing database load.
- 15:30 : OUTAGE ENDS — Service performance returned to normal levels.



Root Cause and Resolution

Root Cause: The issue was caused by a poorly optimized database query that was executed frequently due to a recent code deployment. This query led to the exhaustion of the database connection pool, causing delays and access issues for users.

Resolution: The database team identified the problematic query through log analysis and optimized it by adding appropriate indexes and restructuring the query logic. This optimization reduced the load on the database, allowing the connection pool to recover and service to resume normal operations.

Corrective and Preventative Measures

Improvements:

- Enhance the code review process to identify potential database query issues before deployment.
- Implement more granular monitoring for database query performance to detect similar issues early.

Action Items:

- Conduct a post-deployment review: Analyze recent code changes for potential performance issues.
- Add query performance monitoring: Implement monitoring tools to track query execution times and resource usage.
- Update database connection pool settings: Increase the pool size and implement better connection management practices.
- Schedule regular database optimization reviews: Periodically review and optimize database queries and indexes.
- Train development team: Conduct workshops on writing efficient database queries and understanding their impact on performance.

By addressing these areas, we aim to prevent similar incidents in the future and ensure a more robust and reliable service for our users.

