---
title: Create IP filter criteria
<<<<<<< HEAD
description: Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the SQL API ODBC or JDBC driver. By default, all incoming IPs are blocked until you configure the SQL API Authentication Policy with an IP filter and policy condition to allow access only from trusted client machines.
locale: en-us
=======
description: Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the Live Connect ODBC/JDBC driver.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/create-ip-filter-criteria.html
>>>>>>> refs/remotes/origin/australia
release: australia
product: Web Services
classification: web-services
topic_type: task
<<<<<<< HEAD
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure SQL API plugin on your ServiceNow instance, Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
=======
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Live Connect configuration on your ServiceNow instance, Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
>>>>>>> refs/remotes/origin/australia
---

# Create IP filter criteria

<<<<<<< HEAD
Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the SQL API ODBC or JDBC driver. By default, all incoming IPs are blocked until you configure the SQL API Authentication Policy with an IP filter and policy condition to allow access only from trusted client machines.

## Before you begin

-   Consult your network team to identify the IP address range for your ODBC or JDBC client machines. Depending on your network configuration and where the client machine is located in your network, it may be necessary to allow the external IP address rather than the internal IP address.
-   Complete the previous configuration steps: creating a Service Account and configuring Access Control Lists \(ACLs\).
=======
Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the Live Connect ODBC/JDBC driver.

## Before you begin

-   Consult your network team to identify the IP address range for your ODBC or JDBC client machines. You may need to use the external IP address rather than the internal IP address, depending on your network configuration.
-   Complete the configuration steps:
    -   [Assign roles and create service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/create-service-account.md)
    -   [Create Access Control Lists \(ACLs\) for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/create-acls-sql-api.md)
>>>>>>> refs/remotes/origin/australia

Role required: admin

## About this task

<<<<<<< HEAD
This is the third and final configuration procedure for enabling SQL API access on your instance. After completing this task, your Service Account will be able to connect to ServiceNow via ODBC or JDBC from the specified IP addresses and query the tables for which access has been granted.

By default, all incoming IP addresses are blocked for SQL API connections. You must explicitly define which IP addresses or IP ranges are permitted to connect. This ensures that only trusted client machines can access your ServiceNow data through the SQL API.

**Note:** For additional details on IP filtering, refer to the [IP filter documentation](https://www.servicenow.com/docs/r/platform-security/authentication/create-ip-filter-criteria.html) in the ServiceNow Platform Security guide.

## Procedure

1.  Navigate to the **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **All Policies**.

2.  Search for **SQL API Authentication Policy** and open it.

3.  From the **Policy Inputs** tab, select **New**.

    ![UI screen showing SQL API Authentication Policy.](../image/sql-api-auth-policy-new.png)

4.  A screen appears asking "What kind of Policy Input \(Filter Criteria\) do you want to create?" Select **IP Filter Criteria**.

5.  Provide a Name and Description to identify this IP network or filter group.

6.  From the **IP Range** tab, double-click \(or use the keyboard shortcut\) **Insert a new row**.

    ![UI screen example showing IP filter criteria.](../image/sql-api-IP-filter-criteria.png)

7.  Define the specific IP addresses or IP address ranges your ODBC/JDBC client machines that should be allowed to connect to your ServiceNow instance via the SQL API drivers.

    Enter the outbound IP address, not the internal IP address. Your IT team should be able to provide this information. BI tools and analytics platforms connect from these machines to your to ServiceNow instance.

8.  Select **Submit**.

9.  Go to the **Policy Conditions** tab and select **New**.

    After defining the IP filter criteria and range, add a Policy Condition to the SQL API Authentication Policy to enforce the IP restriction for ODBC or JDBC access.

10. Provide a Name and Description of this Policy condition.

11. Create a filter condition.

    A filter condition is a logical combination of policy inputs \(filter criteria\) to evaluate authentication requests. For example, choose the name of the IP Filter Criteria created earlier and give a condition as shown in the following example diagram.![UI screen example showing how to create a filter condition.](../image/sql-api-policy-condition.png)

12. Select **Submit**.
=======
By default, all incoming IP addresses are blocked for Live Connect connections. To allow access only from trusted client machines, configure the Authentication Policy with an IP filter and policy condition.

**Note:** For additional details on IP filtering, see [IP Filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/ip-filter.md) in the ServiceNow Platform Security guide.

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **All Policies**.

2.  Search for **Live Connect Authentication Policy** and open it.

3.  From the **Policy Inputs** tab, select **New**.

    A dialog appears prompting you to select a policy input type.

    If the dialog does not appear, verify that you selected **New** from the **Policy Inputs** tab and not from another section of the form.

4.  Select **IP Filter Criteria**.

5.  On the IP Filter Criteria form, enter the following information:

    -   **Name**: Enter a name to identify this IP filter group \(for example, AllowedIPRange\).
    -   **Description**: Enter a description \(for example, Allowed IP addresses for ODBC/JDBC connections\).
6.  From the **IP Range** tab, double-select the **Start IP** column to insert a new row.

    Enter the IP address range for ODBC/JDBC client machines that are allowed to connect:

    -   **Start IP**: Enter the starting IP address of the range.
    -   **End IP**: Enter the ending IP address of the range. For a single IP address, enter the same value in both Start IP and End IP.
    -   **Description**: Enter a description.
    The IP addresses you enter are the outbound IP addresses, not the internal IP addresses. Your IT team can provide this information. These are the machines from which BI tools and analytics platforms will connect to ServiceNow.

7.  Select **Submit**.

    The page returns to the Live Connect Authentication Policy form.

    If the page does not return to the Live Connect Authentication Policy form, check that all required fields are filled in and resubmit.

8.  Select the **Policy Conditions** tab and select **New**.

9.  On the Condition form, enter the following information:

    -   **Label**: Enter a label to identify this policy condition \(for example, AllowedIPs\).
    -   **Description**: Enter a description of this policy condition \(for example, Allowed IPs for ODBC\).
10. In the Condition section, select **Add Filter Condition**.

    -   From the first drop-down list, select the name of the IP filter criteria you created earlier.
    -   From the second drop-down list, select **is**.
    -   From the third drop-down list, select **true**
11. Select **Submit**.

    The condition appears in the Policy Conditions list on the Live Connect Authentication Policy form.

    If the condition does not appear in the list, verify that all fields in the Condition form are filled in correctly and resubmit.
>>>>>>> refs/remotes/origin/australia


## Result

<<<<<<< HEAD
You have successfully configured IP filtering for SQL API access. Your ServiceNow instance will now accept SQL API connections only from the specified IP addresses or IP ranges. All other connection attempts will be blocked by default.

Your Service Account can now connect to ServiceNow via ODBC or JDBC from the permitted client machines and query the tables for which both egress\_sql and read ACLs have been configured.

**Parent Topic:**[Configure SQL API plugin on your ServiceNow instance](configure-sql-api-overview.md)
=======
You have successfully configured IP filtering for Live Connect access. Your ServiceNow instance accepts Live Connect connections only from the specified IP addresses or IP ranges. All other connection attempts are blocked by default.

Your user account can connect to ServiceNow via ODBC or JDBC from the permitted client machines.

**Parent Topic:**[Live Connect configuration on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configure-sql-api-overview.md)
>>>>>>> refs/remotes/origin/australia

