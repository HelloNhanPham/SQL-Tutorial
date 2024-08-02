# PERFORMANCE TUNING

**SQL Performance tuning** is the process of enhancing SQL queries to speed up the server performance. Performance tuning in SQL shortens the time it takes for a user to receive a response after sending a query and utilizes fewer resources in the process. The idea is that users can occasionally produce the same intended result set with a faster-running query.
<code>SQL performance tuning is speeding up queries against a relational database.</code>
It is a very important concept if you are pursuing SQL as your career. Many companies ask about SQL performance tuning in interview questions, as optimizing database speed is a priority for everyone.
In this article, we discuss various tools and techniques to increase SQL performance and learn each technique step by step.
## Table of Content
- Factors Affecting SQL Speed
- Ways to Find Slow SQL Queries in SQL Server
- Performance Tuning in SQL Query
- Index Tuning
- SQL Performance Tuning Tools
## Factors Affecting SQL Speed
Some of the major factors that influence the computation and execution time in SQL are:
- **Table size**: Performance may be impacted if your query hits one or more tables with millions of rows or more.
- **Joins**: Your query is likely to be slow if it joins two tables in a way that significantly raises the number of rows in the return set.
- **Aggregations**: Adding several rows together to create a single result needs more processing than just retrieving those values individually.
- **Other users executing queries**: The more queries a database has open at once, the more it must process at once, and the slower it will all be. It can be particularly problematic if other users are using a lot of resources to perform queries that meet some of the aforementioned requirements.
## Ways to Find Slow SQL Queries in SQL Server
**1. Create an Execution Plan**: It is essential to be able to create execution plans, which you can accomplish with SQL Server Management Studio, in order to diagnose delayed queries. After the queries run, actual execution plans are generated. To create an execution plan:
- Start by selecting “Database Engine Query” from the toolbar of SQL Server Management Studio.
- Enter the query after that, and then select “Include Actual Execution Plan” from the Query option.
- It’s time to run your query at this point. You can do that by pressing F5 or the “Execute” toolbar button.
- The execution plan will then be shown in the results pane, under the “Execution Pane” tab, in SQL Server Management Studio.
**2. Monitor Resource Usage**: The performance of a SQL database is greatly influenced by resource use. Monitoring resource use is important since you can’t improve what you don’t measure. Use the System Monitor tool on Windows to evaluate SQL Server’s performance. You may view SQL Server objects, performance counters, and other object activity with it. Simultaneously watch Windows and SQL Server counters with System Monitor to see if there is any correlation between the two services’ performance.
**3. Use SQL DMVs to Find Slow Queries**: The abundance of dynamic management views (DMVs) that SQL Server includes is one of its best features. There are many of them, and they may offer a lot of knowledge on a variety of subjects.
Various DMVs are available that offer information on query stats, execution plans, recent queries, and much more. These can be combined to offer some incredible insights.
