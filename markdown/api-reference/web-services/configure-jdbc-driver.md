---
<<<<<<< HEAD
title: Configure ServiceNow SQL API JDBC driver on client machine
description: Configure the JDBC driver settings on your client machine to establish a connection to your ServiceNow instance and access data through the SQL API.
locale: en-us
=======
title: Configure ServiceNow Live Connect JDBC driver on a client machine
description: Configure the JDBC driver to connect to your ServiceNow instance and query your data.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/configure-jdbc-driver.html
>>>>>>> refs/remotes/origin/australia
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
<<<<<<< HEAD
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure ServiceNow SQL API JDBC driver on client machine

Configure the JDBC driver settings on your client machine to establish a connection to your ServiceNow instance and access data through the SQL API.

## Before you begin

Verify the following prerequisites are met:

-   You have downloaded the ServiceNow SQL API JDBC driver to your client machine. See [Download the SQL API drivers on client machine](download-sql-api-drivers.md) for more information.
-   JDK 17 is installed on your client machine.
-   You have valid ServiceNow credentials for a Service Account with the required roles assigned. See [Create a Service Account and assign Roles](create-service-account.md) for more information.
-   Your client machine's IP address is included in the SQL API IP filter criteria. See [Create IP filter criteria](create-ip-filter-criteria.md) for more information.
-   You have the necessary connection parameters including your ServiceNow instance URL and Service Account credentials.

Role required: local administrator on client machine for installation

## About this task

After configuring the JDBC driver, your applications can execute SQL queries against authorized ServiceNow tables through the SQL API.

## Procedure

1.  Locate the downloaded ServiceNow JDBC driver JAR file on your client machine.

    The driver file is typically named `servicenow-jdbc-driver.jar` or similar.

2.  Add the JDBC driver to your application's classpath or configure it in your BI tool's driver management section.

    The method for adding the driver varies depending on your application. Consult your BI tool's documentation for specific instructions on adding custom JDBC drivers.

3.  Configure the JDBC connection URL using the following format:
=======
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure ServiceNow Live Connect JDBC driver on a client machine

Configure the JDBC driver to connect to your ServiceNow instance and query your data.

## Before you begin

Verify the following:

-   The ServiceNow Live Connect JDBC driver is downloaded. See [Download the Live Connect drivers on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/download-sql-api-drivers.md).
-   JDK 17 is installed.
-   A valid ServiceNow user account \(personal or service account\) with the required roles. See [Assign roles and create service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/create-service-account.md).
-   The client machine IP address is included in the Live Connect IP filter criteria. See [Create IP filter criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/create-ip-filter-criteria.md).
-   The ServiceNow instance URL and user account credentials \(personal or service account\) must be available.
-   OAuth Application Registry must be configured if you plan to connect using OAuth instead of basic authentication. See [Enable OAuth for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/enable-oauth-for-live-connect.md).

Role required: admin

## Procedure

1.  Locate the ServiceNow JDBC driver JAR file on your client machine.

    The file is typically named `servicenow-jdbc-driver.jar`.

2.  Add the JDBC driver to your application's classpath or configure it in your BI tool's driver management section.

    The method varies by application. Consult your BI tool documentation for instructions.

3.  Configure the JDBC connection URL:
>>>>>>> refs/remotes/origin/australia

    ```
    jdbc:servicenow://https://<instance-name>.service-now.com
    ```

<<<<<<< HEAD
    For example, `jdbc:servicenow://https://exampleinstance.service-now.com`.

4.  Enter the Service Account credentials:

    -   **Username**: Enter the User ID of the Service Account with the sn\_jdbc\_rest\_access role.
    -   **Password**: Enter the password for the Service Account.
5.  Test the connection to confirm that the JDBC driver can successfully connect to your ServiceNow instance.

    Most BI tools and database clients provide a **Test Connection** button. Use this feature to validate your configuration before proceeding.
=======
    Example:

    ```
    jdbc:servicenow://https://exampleinstance.service-now.com
    ```

4.  Select an authentication method and configure the driver properties.

<table id="choicetable_cry_fmy_hkc"><tbody><tr><td id="d650928e205">

**Method**

</td><td>

Properties

</td></tr><tr><td id="d650928e214">

**Basic Authentication**

</td><td>

Set **user** to the user ID with the **sn\_jdbc\_rest\_access** role and **password** to the user password. For personal user accounts using basic authentication, the **snc\_basic\_auth\_api\_access** role must also be assigned.

</td></tr><tr><td id="d650928e235">

**OAuth**

</td><td>

Set **useoauth** to `true` and provide the OAuth properties described in [OAuth connection properties for ODBC and JDBC drivers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/oauth-connection-properties-for-odbc-and-jdbc-drivers.md).

</td></tr></tbody>
</table>5.  To verify the connection, test that the JDBC driver connects to your ServiceNow instance.

    Most BI tools and database clients provide a **Test Connection** button.

    A confirmation message appears if the connection is successful.
>>>>>>> refs/remotes/origin/australia


## Result

<<<<<<< HEAD
After successfully configuring the JDBC driver, your BI tool or application can connect to ServiceNow and execute SQL queries against authorized tables. You can now query ServiceNow data directly without requiring data export or replication.

**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)
=======
The JDBC driver is configured. Your BI tool or application can connect to ServiceNow and execute SQL queries against authorized tables.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configuring-sql-api.md)
>>>>>>> refs/remotes/origin/australia

