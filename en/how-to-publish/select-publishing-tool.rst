Select a publishing tool or service
^^^^^^^^^^^^^^^^^^^^^^^^

There are a number of different tools and services available to help organisations create their IATI xml files. The tools and services options offer different levels of support, automation and pricing. Do have a look through the summaries below when deciding what publishing option is best for your organisation.

Available publishing tools:
>>>>>>>>>>>>>>>>>>>>>>
>>>>>>>>>>>>>>>>>>>>>

The following tools and services are currently available to organisations to start using:

Aidstream
=========

Aidstream (http://www.aidstream.org) is a free online data entry and management tool which you use by manually entering all of the relevant activity information through the use of drop-down menus, text boxes or CSV upload. Aidstream converts the data entered into XML and outputs both organisation and activity data files for publishing, as well as importing previously published XML. The data stored in Aidstream can be added to or amended at any point. Manual data on Aidstream is usually the tool of choice if you only have a small number of activities (approx < 15 - 20) to publish; the CSV upload function allows you to add 100+ activities more easily.

More information about the tool can be found `here <https://github.com/younginnovations/aidstream/wiki/User-Guide>`__. For general enquiries please contact: support@aidstream.org.

Akvo RSR
=========================

`Akvo Really Simple Reporting <http://akvo.org/products/rsr/#overview>`__ (RSR) is an online platform for reporting, monitoring, and publicly communicating international development programs. Features include management, tracking, and updating of projects from the desk or remotely, and RSR enables users to automatically push or pull data to or from the IATI registry.

More information about pricing can be found `here <http://akvo.org/products/rsr/#pricing>`__. For general enquiries, `contact Akvo <http://akvo.org/get-in-touch/>`__.

Spreadsheet2IATI Service
=========================

The Spreadsheet2IATI service is a tool that makes producing valid IATI data easy and accessible, streamlining the reporting process. 

The service has been running successfully since May 2017. It offers standardized spreadsheets templates (e.g. in Excel format) you can use and update with your information. The converter reads the spreadsheets, checks if they are valid, and produces the XML files. You receive feedback on the data quality and insight in what is included, to check for completeness. Think of it as your accountant or payroll service: for each quarterly or monthly update, you provide the raw information, and we compile the IATI file with additional advice for data quality improvement. You remain in control of the process, choosing to publish directly via the tool or to upload the information yourself. 

More information about the service and pricing can be found `here <https://data4development.nl/wp-content/uploads/2017/09/Product-page-Spreadsheet2IATI-Converter-1.pdf>`__. For general enquiries, contact: info@data4development.nl.

Upcoming publishing tools and services:
>>>>>>>>>>>>>>>>>>>>>>
>>>>>>>>>>>>>>>>>>>>>>>

These are tools and services that are currently in development and testing phase. They will soon be available to organisations.

CoVE
====================

CoVE is an web application to Convert, Validate and Explore data following certain open data standards - currently 360Giving and the Open Contracting Data standard. The Open Data Services Team are updating it to work with the IATI Data Standard. The tool will allow organisations to transform CSV files into IATI XML.

More information can be found `here <http://cove.opendataservices.coop>`__. For general enquiries, `contact Open Data Services <http://www.opendataservices.coop/>`__.

IATI Studio Publisher
====================

`IATI Studio Publisher <https://www.iatistudio.com/>`__ allows for validated IATI publication, both on activity level and organisation level. Drafted data will be available before the user chooses to export the data to a valid XML file and the service is integrated with the IATI Studio Chart Builder and Micro-site Builder, more details of which can be `found here <https://www.iatistudio.com/features/>`__.

Core functionality is free; more information about pricing in premium packages can be found `here <https://www.iatistudio.com/membership/>`__. For general enquiries, `contact the IATI Studio team <https://www.iatistudio.com/support/>`__.

Bespoke (In House Applications):
>>>>>>>>>>>>>>>>>>>>>>
>>>>>>>>>>>>>>>>>>>>>

Organisations with internal technical expertise and capacity may decide to generate their own mechanisms for converting their data into IATI data. This can be done by developing internal systems and processes so that data is pulled together from internal management and finance systems to create XML data. This requires technical knowledge of both XML and the organisation's internal systems in order to create a programme to achieve this. This can be done with either internal technical expertise or by bringing in consultants to develop a bespoke package.

This is normally an option often chosen by large organisations reporting a large number of activities, as in the long-run this proves to be a more cost effective means of reporting to IATI.

One example of how an organisation has created a bespoke publishing system is DFID's SQL-To-IATI: 

SQL-To-IATI
==============

The `SQL-to-IATI tool <https://github.com/DFID/SQL-to-IATI-Database>`__ generates IATI XML data from activity data stored in a SQL database. DFID use this to publish their full set of 13000 activities each month, so it supports enterprise-grade IATI.

The core of the database is the IATI schema which contains a set of tables that mirror the IATI 2.01 standard XML schema in a relational database. The data held in these tables can be output as valid IATI XML files directly from a SQL function.

DFID are willing to share the codebase with organisations as they seek to publish more data to the IATI standard, and the code is freely available on GitHub. They would like to partner with others interested in developing this further as an open source tool for the IATI community. Contact DFID’s Technical Transparency Team: devtracker-feedback@dfid.gov.uk if you are interested.

__________________


**Note:** *If you are a provider of an IATI tool or service and would like to add or update information on this page. Please create a pull request on* `Github <https://github.com/IATI/IATI-Guidance/edit/master/en/how-to-publish/select-publishing-tool.rst>`__. *Alternatively please contact the IATI Technical Support Team at: support@iatistandard.org.*
