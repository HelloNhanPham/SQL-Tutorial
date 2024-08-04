# Window functions

Window functions apply to aggregate and ranking functions over a particular window (set of rows). OVER clause is used with window functions to define that window. OVER clause does two things : 

- Partitions rows to form a set of rows. (PARTITION BY clause is used) 
- Orders rows within those partitions into a particular order. (ORDER BY clause is used)

**Note**: If partitions aren’t done, then ORDER BY orders all rows of the table. 

**Syntax**

```sql
SELECT column_name1, window_function(cloumn_name2)
OVER([PARTITION BY column_name1] [ORDER BY column_name3]) AS new_column
FROM table_name;
```

**Parameters**

>
> window_function = any aggregate or ranking function    
> column_name1 = column to be selected
> column_name2 = column on which window function is to be applied
> column_name3 = column on whose basis partition of rows is to be done
> new_column = Name of new column
> table_name = Name of table

## Aggregate Window Function
Various aggregate functions such as SUM(), COUNT(), AVERAGE(), MAX(), and MIN() applied over a particular window (set of rows) are called aggregate window functions. 

