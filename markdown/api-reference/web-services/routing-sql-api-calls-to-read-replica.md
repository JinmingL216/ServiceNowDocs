---
<<<<<<< HEAD
title: Route SQL API calls to Read Replica
description: You can route SQL API calls to Read Replica to optimize the performance of your ServiceNow instance.
locale: en-US
=======
title: Route Live Connect calls to Read Replica
description: Route Live Connect calls to a Read Replica database to reduce the processing load on the primary database in your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/routing-sql-api-calls-to-read-replica.html
>>>>>>> refs/remotes/origin/australia
release: australia
product: Web Services
classification: web-services
topic_type: task
<<<<<<< HEAD
last_updated: "2026-03-15"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Route SQL API calls to Read Replica

You can route SQL API calls to Read Replica to optimize the performance of your ServiceNow instance.

## Before you begin

You must have a secondary database configured for your ServiceNow instance.
=======
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Route Live Connect calls to Read Replica

Route Live Connect calls to a Read Replica database to reduce the processing load on the primary database in your ServiceNow instance.

## Before you begin

A secondary database must be configured for your ServiceNow instance.
>>>>>>> refs/remotes/origin/australia

Role required: admin

## About this task

<<<<<<< HEAD
Query routing takes the load off the primary database for SELECT queries that take numerous DB CPU cycles on the primary DB. For more information, see [Introduction to ServiceNow Read Replica Databases](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824441).
=======
Query routing directs SELECT queries to a Read Replica database instead of the primary database, reducing the processing load on the primary database. For more information, see [Introduction to ServiceNow Read Replica Databases](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824441) \(KB0824441\).
>>>>>>> refs/remotes/origin/australia

## Procedure

1.  Navigate to **All** &gt; **Secondary Database** &gt; **Secondary Database Category**.

<<<<<<< HEAD
2.  Select **New** to create secondary database category for ODBC/JDBC.

3.  In the Name field, enter **odbc** or **jdbc**.

    Don't change any other field on this page. If you must change the default values, first refer to this KB: [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0824441](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824441) ![UI screen example for creating secondary database category.](../image/sql-api-read-replica.png)

4.  Select **Map All Pools** to map the database pools to this category.

5.  Select the database pools to be added.

    The selected pools appear under the **Member Secondary Database Pools**.

6.  Select **Save**.


**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)
=======
2.  Select **New**.

    This creates a secondary database category for ODBC/JDBC.

3.  In the **Name** field, enter **odbc** or **jdbc**.

    **Warning:** Don't change any other field on this form. If you must change the default values, review the [Introduction to ServiceNow Read Replica Databases](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824441) \(KB0824441\) article in the Now Support Knowledge Base before making changes.

4.  Select **Map All Pools**.

    This maps the database pools to this category.

5.  Select the database pools to add.

    The selected pools appear in the **Member Secondary Database Pools** list.

6.  Select **Update**.


**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configuring-sql-api.md)
>>>>>>> refs/remotes/origin/australia

