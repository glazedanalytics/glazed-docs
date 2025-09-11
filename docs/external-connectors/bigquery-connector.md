# Connect to Google BigQuery using a Service Account

Connect Glazed to Amazon Redshift to validate your analytics events in real-time.

> A service account enables Glazed to automatically validate that the events you create on the Glazed App are correctly arriving to your data warehouse.
>
> This is a read-only service and we will only store the last timestamp for each event (i.e. “last seen) and the aggregated last 30-day volume (total number of clicks).

## Prerequisites

Before connecting BigQuery to Glazed, ensure you have:

- **Google Cloud Project**: Access to a Google Cloud Console project where your BigQuery data is stored
- **Project Admin Rights**: IAM permissions to create service accounts and assign roles
- **BigQuery Access**: The project must have BigQuery enabled and contain your analytics data
- **Data Location**: Know which datasets and tables contain your event data

## Setup Process

### 1. Create User in BigQuery

1. Open the [Google Cloud Console](https://console.cloud.google.com/) and select your project.
2. Navigate to the "IAM & Admin" section in the left sidebar.

   ![BigQuery Step 1](images/big-query-connect-0.png)

3. Click on "[Service Accounts"](https://console.cloud.google.com/iam-admin/serviceaccounts) and then on "Create Service Account".

   ![BigQuery Step 2](images/big-query-connect-1.png)

4. Choose a name (e.g. Glazed Analytics) and description for your service account and click on "Create and Continue".

   ![BigQuery Step 3](images/big-query-connect-2.png)

5. Under "Role", select "BigQuery" and then "BigQuery Data Viewer" and "BigQuery Job User".
6. Click on "Done".

   ![BigQuery Step 4](images/big-query-connect-3.png)

7. Click on the vertical dots on the right of your service account and select "Manage Keys".

   ![BigQuery Step 5](images/big-query-connect-4.png)

8. Click on “Add Key” and then “Create new key”.

   ![BigQuery Step 6](images/big-query-connect-5.png)

9. Choose "JSON" as the key type and click on "Create".

   ![BigQuery Step 7](images/big-query-connect-6.png)

10. Save the JSON file to a secure location on your local machine.

🥳 You have now created a Google BigQuery service account with Data Viewer and Job User roles and downloaded the API key file. After completing the connection process Glazed can use this account to access BigQuery through the API.

### 2. Connect Glazed to Table

Inside a project or design file:

1. Click on the DB icon in the top navigation bar
2. Select your DWH connector
   ![DW connector in Glazed](images/DW-glazed-1.png)

3. Add the connection details (from above process)
4. Specify the corresponding schema and column names (Amplitude, Mixpanel, Custom)
   ![DW connector Schema](images/DW-glazed-2.png)
