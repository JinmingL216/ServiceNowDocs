---
<<<<<<< HEAD
title: Common use cases for SQL API
description: The SQL API supports business intelligence reporting, ad-hoc data analysis, and custom report development.
locale: en-US
=======
title: Use cases for Live Connect
description: Live Connect supports business intelligence \(BI\) reporting, ad-hoc data analysis, and custom report development.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/common-use-cases-for-sql-api.html
>>>>>>> refs/remotes/origin/australia
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [use]
<<<<<<< HEAD
breadcrumb: [Explore, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Common use cases for SQL API

The SQL API supports business intelligence reporting, ad-hoc data analysis, and custom report development.

The SQL API is particularly useful for scenarios that require direct access to ServiceNow data from external tools and platforms. These use cases demonstrate how organizations leverage SQL API to enhance their data analysis and reporting capabilities.
=======
breadcrumb: [Explore, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Use cases for Live Connect

Live Connect supports business intelligence \(BI\) reporting, ad-hoc data analysis, and custom report development.

The Live Connect is particularly useful for scenarios that require direct access to ServiceNow data from external tools and platforms. These use cases demonstrate how organizations use Live Connect to enhance their data analysis and reporting capabilities.
>>>>>>> refs/remotes/origin/australia

## Business intelligence and reporting

Connect your preferred BI tools to create dashboards and reports that combine ServiceNow data with information from your other business systems. You can build comprehensive views that span multiple data sources without copying ServiceNow data to external systems.

<<<<<<< HEAD
This use case enables you to integrate standard BI platforms such as Tableau, Power BI, Looker, and other ODBC/JDBC-compatible tools directly with your ServiceNow data, eliminating the need for data export or replication.
=======
This use case enables you to integrate standard BI platforms such as Pyramid Analytics, Tableau, Power BI, and other ODBC/JDBC-compatible tools directly with your ServiceNow data, eliminating the need for data export or replication.
>>>>>>> refs/remotes/origin/australia

## Ad-hoc data analysis

Run exploratory queries to investigate trends, identify patterns, or troubleshoot issues with minimal impact on your ServiceNow instance's performance. No administrator intervention is required.

<<<<<<< HEAD
By writing targeted SQL queries, you can retrieve only the data you need. This reduces network overhead and improves performance. The pass-through query support enables you to apply WHERE clauses, perform aggregations, and join multiple ServiceNow tables in a single query.
=======
By writing targeted SQL queries, you can retrieve only the data you need. This reduces network overhead on data pipeline and data transformation, improving performance. The pass-through query support enables you to apply WHERE clauses, perform aggregations, and join multiple ServiceNow tables in a single query.
>>>>>>> refs/remotes/origin/australia

## Custom report development

Build specialized reports using your organization's standard reporting tools and frameworks. You can maintain control over report design and scheduling while accessing live ServiceNow data.

<<<<<<< HEAD
The SQL API supports read-only operations that avoid unintended modifications to your ServiceNow records. This ensures that your analytical work cannot accidentally modify production data. This helps provide a secure environment for developing and executing custom reports.

## External data source integration

SQL API is designed with built-in limits to keep your ServiceNow instance running smoothly. You can use it to query specific data and integrate it with other data sources, as long as you stay within these limits.

**Parent Topic:**[Getting started with ServiceNow SQL API](getting-started-with-servicenow-sql-api.md)
=======
Live Connect supports read-only operations that avoid unintended modifications to your ServiceNow records. This ensures that your analytical work can't accidentally modify production data. This helps provide a secure environment for developing and executing custom reports.

## External data source integration

Live Connect is designed with built-in limits to keep your ServiceNow instance running smoothly. You can use it to query specific data. Your client applications can combine this data and integrate it with other data sources, as long as you stay within these the Live Connect query limits. For information on query limits, see [Usage limitations for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/usage-limitations.md).

**Parent Topic:**[Getting started with ServiceNow Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/getting-started-with-servicenow-sql-api.md)
>>>>>>> refs/remotes/origin/australia

