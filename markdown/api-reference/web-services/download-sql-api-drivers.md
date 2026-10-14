---
<<<<<<< HEAD
title: Download the SQL API drivers on client machine
description: Download the ODBC and JDBC drivers from the ServiceNow store to your client machine to enable SQL API connectivity.
locale: en-us
=======
title: Download the Live Connect drivers on a client machine
description: Download ODBC and JDBC drivers to enable third-party Business Intelligence tools and data analysis platforms to connect to your ServiceNow instance data.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/download-sql-api-drivers.html
>>>>>>> refs/remotes/origin/australia
release: australia
product: Web Services
classification: web-services
topic_type: task
<<<<<<< HEAD
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Download the SQL API drivers on client machine

Download the ODBC and JDBC drivers from the ServiceNow store to your client machine to enable SQL API connectivity.

## Before you begin

Role required: admin

## About this task

After configuring the SQL API plugin on your ServiceNow instance, you must download the ODBC and JDBC drivers to your client machine. These drivers enable your Business Intelligence tools and data analysis platforms to connect to your ServiceNow data.

## Procedure

1.  Go to [ServiceNow Store](http://store.servicenow.com).

2.  Search for `SQL API`.

    The SQL API Drivers page appears.

3.  Select **Get**.

    The ServiceNow SQL API Driver ZIP file is downloaded on your client machine.

    The ZIP file contains two folders:

    -   `ServiceNow SQL API- ODBC driver`: This folder contains the ODBC driver executables for both 32-bit and 64-bit architectures, and a dependencies folder with JAR files.
    -   `ServiceNow SQL API- JDBC driver`: This folder contains the JDBC driver JAR files.

## Result

The SQL API drivers are downloaded to your client machine and ready for installation and configuration.

## What to do next

After downloading the drivers, proceed to install and configure them on your client machine.

-   For ODBC driver installation, see [Install ServiceNow SQL API ODBC driver on client machine](install-odbc-driver.md).
-   For JDBC driver configuration, see [Configure ServiceNow SQL API JDBC driver on client machine](configure-jdbc-driver.md).

**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)
=======
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Download the Live Connect drivers on a client machine

Download ODBC and JDBC drivers to enable third-party Business Intelligence tools and data analysis platforms to connect to your ServiceNow instance data.

## Before you begin

Verify that your client machine meets the following requirements:

|Requirement|Description|
|-----------|-----------|
|Operating system|Windows with administrator permissions. For supported versions and troubleshooting guidance, see [Troubleshooting Live Connect — Connection, Authentication, and Query Errors](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2917911) \[KB2917911\] in the Now Support Knowledge Base.|
|Java Development Kit \(JDK\)|JDK 17. Using a different JDK version may cause installation or configuration issues.|
|Microsoft Visual C++ Redistributable|Required dependency for the ODBC driver.|

Role required: admin

## Procedure

1.  Navigate to [store.servicenow.com](https://store.servicenow.com).

2.  Search for `Live Connect`.

    The Live Connect tile appears in the search results.

3.  Select Live Connect.

    The download page appears.

    If the download page does not appear, verify that you selected the correct tile in the search results.

4.  Select **Download**.

    The ZIP file contains the following folders:

    |Folder|Contents|
    |------|--------|
    |`ServiceNow Live Connect - ODBC driver`|ODBC driver executables for 32-bit and 64-bit architectures, and a dependencies folder with BCFIPS JAR files.|
    |`ServiceNow Live Connect - JDBC driver`|JDBC driver JAR files.|


## Result

The Live Connect drivers are downloaded to your client machine and ready for installation and configuration.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configuring-sql-api.md)
>>>>>>> refs/remotes/origin/australia

