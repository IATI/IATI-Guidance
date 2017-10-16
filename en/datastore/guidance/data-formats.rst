Data Formats
============

All IATI data is provided by publishers in XML format. The Datastore is able to automatically convert the published data into two other formats (JSON and CSV). Each of these has a range of benefits and limitations.

By default, data is filtered and output based on `activities <http://iatistandard.org/activity-standard/overview/iati-activity/>`__.

When outputting data in CSV format you can instead choose to display data based on `budgets <http://iatistandard.org/activity-standard/overview/budgets/>`__ or `transactions <http://iatistandard.org/activity-standard/overview/transactions/>`__.

XML
---

The Datastore returns the original activity XML as published. This is `enhanced with metadata <http://iatistandard.org/guidance/datastore/reference/structure-of-data/>`__ specifying the version that individual activities were published at, as well as details of the query result.

JSON
----

The Datastore will convert the published XML to a JSON format. All of the originally published information is present in this alternative format. The same `metadata <http://iatistandard.org/guidance/datastore/reference/structure-of-data/>`__ that is given in the XML output is available in the JSON output.

CSV
---

The Datastore will convert the published XML data into CSV format. Only a subset of published data is present. This format can be used to analyse information using spreadsheet software such as Microsoft Excel or Libreoffice Calc.

Rows in a CSV file may represent individual activities, budgets or transactions depending on the output format that is selected. Each of these may be expanded by sector or country so that percentage splits may be analysed.
