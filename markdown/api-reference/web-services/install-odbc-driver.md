---
<<<<<<< HEAD
title: Install ServiceNow SQL API ODBC driver on client machine
description: Install the ServiceNow ODBC driver on your Windows client machine to enable connectivity between your Business Intelligence \(BI\) tools and ServiceNow data through the SQL API.
locale: en-us
=======
title: Install the ServiceNow Live Connect ODBC driver on a client machine
description: Use the installation wizard to install the ODBC driver and configure the connection between your Business Intelligence tools and ServiceNow data.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/install-odbc-driver.html
>>>>>>> refs/remotes/origin/australia
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
<<<<<<< HEAD
reading_time_minutes: 3
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Install ServiceNow SQL API ODBC driver on client machine

Install the ServiceNow ODBC driver on your Windows client machine to enable connectivity between your Business Intelligence \(BI\) tools and ServiceNow data through the SQL API.

## Before you begin

-   ServiceNow SQL API ODBC driver can only be installed on a Windows client machine.
-   Verify that JDK 17 is installed on your client machine.

Role required: local administrator on client machine for installation, admin on ServiceNow instance for server-side configuration.
=======
reading_time_minutes: 2
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Install the ServiceNow Live Connect ODBC driver on a client machine

Use the installation wizard to install the ODBC driver and configure the connection between your Business Intelligence tools and ServiceNow data.

## Before you begin

-   The client machine meets the system requirements listed in [Download the Live Connect drivers on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/download-sql-api-drivers.md).
-   The OAuth Application Registry is configured if you plan to connect using OAuth instead of basic authentication. See [Enable OAuth for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/enable-oauth-for-live-connect.md).

Role required: local administrator \(client machine installation\), admin \(ServiceNow instance configuration\).
>>>>>>> refs/remotes/origin/australia

## Procedure

1.  Locate the downloaded ODBC driver installation file on your client machine.

<<<<<<< HEAD
2.  Select and hold \(or right-click\) the appropriate installation file based on your BI tool's architecture \(32-bit or 64-bit\) and select **Run as administrator**.

3.  In the ServiceNow ODBC Driver Setup wizard, review the welcome screen and select **Next**.

    ![ODBC driver setup wizard welcome screen.](../image/sql-api-driver-welcome.png)

4.  Read and accept the End User License Agreement \(EULA\), and then select **Next**.

5.  Select the installation directory or accept the default location, and then select **Next**.

    The default installation path is typically `C:\Program Files\ServiceNow\ODBC`. ![ODBC driver setup wizard-choose destination folder.](../image/sql-api-driver-destination.png)

6.  When prompted for the **Service Name**, enter a name to identify the service \(for example, ServiceNow\_ODBC\) and select **Next**.

7.  When prompted for the **Java Virtual Machine Location**, do the following actions:

    1.  Browse to and select the directory where the `jvm.dll` file is located \(usually `C:\Program Files\Java\jdk-17\bin\server`\).

    2.  To skip entering the JDK location during installation, select **Next**.

    **Note:**

    You must enter the `jvm.dll` file location for the ServiceNow SQL API ODBC driver to work.

8.  Add the JDK location now or later.

    In the pop-up window,

    -   To enter the JDK location now, select **Yes**.
    -   To enter the JDK location later, select **No**.
    To enter the JDK location later, access the **Management console** as an administrator and navigate to **Services** &gt; **\(Service\_Name\)** &gt; **Service Settings** &gt; **IP Parameters** and enter the `jvm.dll` file location in the `ServiceJVMLocation` property.

9.  When prompted for the **ODBC Data Source** details, specify the following parameters to create an ODBC data source that can be used to create a Data Source Name \(DSN\).

    This DSN will be used to connect your ODBC driver to the ServiceNow instance.

    |Field|Description|
    |-----|-----------|
    |Data Source Name|Short name to identify this data source|
    |Description|Short description of the driver|
    |Service Name|Enter the same **Service Name** as entered in step 6|
    |Service Data Source|This name will be entered in the **Service Data Source** field when setting the **System DSN** in the **ODBC Data Source Administrator** window|

    Usually, the default values are appropriate.

    ![ODBC driver setup wizard-creation of ODBC data source.](../image/sql-api-odbc-data-source.png)

10. Select the **Program Folder** to create links for the driver, and select **Next**.

    ![ODBC driver setup wizard-select program folder to create ODBC driver link.](../image/sql-api-odbc-folder.png)

11. Start copying driver files to the client machine by selecting **Next**.

12. When prompted, select **Finish** and complete the installation.
=======
2.  Select and hold \(or right-click\) the appropriate installation file based on your BI tool's architecture \(32-bit or 64-bit\), and then select **Run as administrator**.

    The ServiceNow ODBC Driver Setup wizard opens.

    If the wizard does not open, verify that you selected **Run as administrator** and that you have local administrator permissions on the client machine.

3.  Follow the wizard prompts to accept the license agreement and select the installation location.

    The default installation path is `C:\Program Files\ServiceNow\ODBC`.

4.  When prompted for the service name, enter a name to identify the service \(for example, ServiceNow\_ODBC\) and select **Next**.

5.  When prompted for the **Java Virtual Machine Location**, select **Browse** and navigate to the `bin\server` directory of your JDK installation and select the `jvm.dll` file.

    Example path: `C:\Program Files\Eclipse Adoptium\jdk-17.0.19.10-hotspot\bin\server\jvm.dll`

    \[Omitted image "sql-api-jvm-location.png"\] Alt text: Browse for JVM Location dialog showing bin\\server folder structure

    **Note:**

    The `jvm.dll` file location is required for the driver to work. You can enter it now or configure it later by navigating to **ServiceNow Live Connect - ODBC Manager** &gt; **Management Console** &gt; **Services** &gt; **\(Service\_Name\)** &gt; **Service Settings** &gt; **IP Parameters** and entering the path in the **ServiceJVMLocation** property.

6.  When prompted to create the ODBC data source, either accept the default values or customize the following fields:

    |Field|Description|
    |-----|-----------|
    |**Data Source Name**|Name to identify this data source.|
    |**Description**|Description of the data source.|
    |**Service Name**|Service name entered earlier in the wizard.|
    |**Service Data Source**|Data source name used in the ODBC Data Source administrator.|

7.  Accept the default program folder or select a custom location, then select **Next**.

8.  Review the installation summary and select **Next** to begin the installation.

9.  Select **Finish** when the installation is complete.
>>>>>>> refs/remotes/origin/australia


## Result

<<<<<<< HEAD
The installation creates a ServiceNow SQL API – ODBC folder in the Start menu with these links:

-   **Interactive SQL\(ODBC\)**: An interactive SQL command window for directly testing SQL statements.
-   **Management Console**: A Microsoft MMC snap-in for configuring default properties for the ODBC driver.
-   **ODBC Administrator**: A Microsoft ODBC Administrator program. Searchable by the name **ODBC Data Sources \(32-bit/64-bit\)**.

![ODBC driver setup wizard-start menu with ODBC driver links](../image/sql-api-odbc-startmenu.png)

The ServiceNow ODBC driver is installed on your client machine and registered with the Windows ODBC Data Source Administrator. You can proceed to configure the driver with your ServiceNow instance connection details.

## What to do next

After completing the installation, configure the ODBC driver to connect to your ServiceNow instance. For configuration instructions, see [Configure ServiceNow SQL API ODBC driver on client machine](configure-odbc-driver.md).

**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)
=======
The installation creates a ServiceNow Live Connect - ODBC Manager folder in the Start menu with these applications:

-   **Interactive SQL \(ODBC\)**: Interactive SQL command window for testing SQL statements.
-   **Management Console**: Microsoft MMC snap-in for configuring ODBC driver properties.
-   **ODBC Administrator**: Microsoft ODBC administrator program \(searchable as **ODBC Data Sources**\).

The ServiceNow ODBC driver is installed on your client machine and registered with the Windows ODBC Data Source administrator.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configuring-sql-api.md)
>>>>>>> refs/remotes/origin/australia

