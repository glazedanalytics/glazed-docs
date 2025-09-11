# Snowflake Connector

Connect Glazed to Snowflake to validate your analytics events in real-time.

> This connector enables Glazed to automatically validate that the events you create on the Glazed App are correctly arriving to your data warehouse.
>
> This is a read-only service and we will only store the last timestamp for each event (i.e. “last seen) and the aggregated last 30-day volume (total number of clicks).

## Prerequisites

Before setting up the Snowflake connector, ensure you have:

- **Admin rights** to create Snowflake Roles and Users
- **ACCOUNTADMIN** or similar role with user management privileges
- **Access to SQL worksheet** in Snowflake
- **Events flowing** into Snowflake tables

## Setup Process

### 1. Create Glazed User

1. Open new `SQL Worksheet` in Snowflake
2. Edit the below query by adding your corresponding values for:
   - WAREHOUSE_NAME
   - DATABASE_NAME
   - SCHEMA_NAME
   - TABLE_NAME
   - PASSWORD
3. Run the query:

```sql
CREATE ROLE "GLAZED_ANALYTICS";

CREATE USER "GLAZED"
    MUST_CHANGE_PASSWORD = FALSE
    DEFAULT_ROLE = "GLAZED_ANALYTICS"
    PASSWORD = "[PASSWORD]";

GRANT USAGE ON WAREHOUSE "[YOUR WAREHOUSE NAME]" TO ROLE "GLAZED_ANALYTICS";
GRANT USAGE ON DATABASE "[YOUR DATABASE NAME]" TO ROLE "GLAZED_ANALYTICS";
GRANT USAGE ON SCHEMA "[YOUR DATABASE NAME]"."[YOUR SCHEMA NAME]" TO ROLE "GLAZED_ANALYTICS";
GRANT SELECT ON TABLE "[YOUR DATABASE NAME]"."[YOUR SCHEMA NAME]"."[YOUR TABLE NAME]" TO ROLE "GLAZED_ANALYTICS";
GRANT ROLE "GLAZED_ANALYTICS" TO USER "GLAZED";
```

> This query grants the “GLAZED” user permission to run `SELECT` statements **only on the specified table**. You can modify the query to grant access to multiple tables as needed.

### 2. Connect Glazed to table

Inside a project or design file:

1. Click on the DB icon in the top navigation bar
2. Select your DWH connector
   ![DW connector in Glazed](images/DW-glazed-1.png)

3. Add the connection details (from above process)
4. Specify the corresponding schema and column names (Amplitude, Mixpanel, Custom)
   ![DW connector Schema](images/DW-glazed-2.png)

## FAQs

### How do I find my custom values?

- `WAREHOUSE_NAME`
  You can run the query SELECT CURRENT_WAREHOUSE() to see the current warehouse or SHOW WAREHOUSES to preview all warehouses.  
  More info here: https://docs.snowflake.com/en/sql-reference/sql/show-warehouses

- `DATABASE_NAME`, `SCHEMA_NAME`, `TABLE_NAME`
  Tables are usually structured as: database_name.schema_name.table_name.

- `Account Identifier`
  The account identifier has the format <org-name>-<account-name>. You can find it from your dedicated Snowplow login URL, before 'snowflakecomputing.com'

> [!TIP]
> You can also run the query `SELECT CURRENT_ORGANIZATION_NAME(), CURRENT_ACCOUNT_NAME();` to access the Organization and account names directly.  
> More infos here: https://docs.snowflake.com/en/user-guide/admin-account-identifier
