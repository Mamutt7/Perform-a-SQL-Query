# Perform a SQL Query

In this lab activity, you’ll use SELECT and FROM in SQL to return the information you need from a database. You’ll also use the ORDER BY keyword to sequence the information returned by a query based on a specified column.

## Scenario
In this scenario, you have to determine which employee devices must be updated. You also need to investigate user login activity to explore if any unusual activity has occurred.

The information you need is located in the machines and login_attempts tables in the organization database.

Here’s how you’ll do this task: First, you’ll obtain information on the employee devices that must be updated. Next, you’ll examine the login attempts for unusual activity. Finally, you’ll use the ORDER BY keyword to sort the data returned by your SQL queries.

### Task 1. Retrieve employee device data
In this task, you need to obtain information on employee devices because your team needs to update them. The information you need is in the `machines` table in the `organization` database.

First, you need to retrieve all the information about the employee devices.

1. Run the following query to select all device information from the machines table:

```
SELECT *
FROM machines;
```

Next, you want to focus on the email client running on various devices.

Run the following query to select only the `device_id` and `email_client` columns from the `machines` table. 

2. Replace `X` with `device_id` and `Y` with `email_client`:

```
SELECT X, Y FROM machines;
```

Now, you need information on the operating systems used on various devices and their last patch date.

3. Complete the query to return only the `device_id`, `operating_system`, and `OS_patch_date` columns from the machines table. Replace `X`, `Y`, and `Z` with the columns that you need to return:

```
SELECT X, Y, Z FROM machines;
```

### Task 2. Investigate login activity
In this task, you need to analyze the information from the `log_in_attempts` table to determine if any unusual activity has occurred.

First, you need to investigate the locations where login attempts were made to ensure that they’re in expected areas (the United States, Canada, or Mexico).

1. Write a SQL query to select the `event_id` and `country` columns from the `log_in_attempts` table.

Next, you need to check if login attempts were made outside of the organization's working hours.

2. Write a SQL query that selects the `username`, `login_date`, and `login_time` columns from the `log_in_attempts` table.

Now, you need to get a complete picture of all login attempts.

3. Write a SQL query that selects all columns from the `log_in_attempts` table, using a single symbol after the `SELECT` keyword.

### Task 3. Order login attempts data
In this task, you need to use the `ORDER BY` keyword. You'll sequence the data that your query returns according to the login date and time.

First, you need to sort the information by date.

1. Run the following query, which orders `log_in_attempts` data by `login_date`:

```
SELECT *
FROM log_in_attempts
ORDER BY login_date;
```

Now, you need to further organize the previous results by ordering them by `login_time`.

2. Modify the query from the previous step by adding the login time to the `ORDER BY` clause. You must replace `X` with the appropriate column name:

```
SELECT * 
FROM log_in_attempts
ORDER BY login_date, X;
```
