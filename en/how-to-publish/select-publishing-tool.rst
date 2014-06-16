Select a publishing tool
^^^^^^^^^^^^^^^^^^^^^^^^^^^

There are currently three different mechanisms recommended by the IATI Secritariat to convert data into IATI- XML data files. Aidstream and the CSV Convertor are recommended because they are both currently actively maintained with the involvement of the IATI Technical Support Team. 



Aidstream 
=========

Aidstream (http://www.aidstream.org) is an online data entry and management tool which you use by manually entering all of the relevant activity information through the use of drop-down menus and text boxes. Aidstream converts the data entered into XML and outputs both organisation and activity datafiles for publishing . The data stored in Aidstream can be added to or amended at any point. Aidstream is usually the tool of choice if you only have a small number of activities (approx < 15 - 20) to publish.

Specific guidance on the use of Aidstream can be found at http://support.iatistandard.org/entries/27374208-AidStream-Guidance




CSV Converter 
=============

The CSV Convertor tool (http://csv2iati.iatistandard.org/) enables relevant activity information to be pulled from across the organisation into a single CSV file. Data for each activity is stored in a single row in the CSV file with column headings mapping to IATI fields .

Once the CSV file is completed, it is uploaded to the conversion tool and a mapping model is created. Column titles from the CSV file are mapped to IATI fields so that information is picked up from the correct place. Default values for some fields can also be set. Once the mapping exercise is completed, you simply click to convert the data and the tool creates an Activity file (no organisation file) for publishing..

Specific guidance on the use of the CSV Convertor can be found at http://csv2iati.iatistandard.org/docs/user_guide.html. Examples of an input CSV file can be found at http://support.iatistandard.org/entries/27375838-CSV-Convertor-Example-Input-CSV-Files .

It is also recommended that Publishers creating their Activity files via the CSV Converter should also use Aidstream in order to create their organisation files



 
Bespoke (In House Applications)
===============================

Organisations with internal technical expertise and capacity may decide to generate their own mechanisms for converting their data into IATI data. This can be done by developing internal systems and processes so that data is pulled together from internal management and finance systems to create XML data. This requires technical knowledge of both XML and the organisation's internal systems in order to create a programme to achieve this. This can be done with either internal technical expertise or by bringing in consultants to develop a bespoke package. 

This is normally an option often chosen by large organisations reporting a large number of activities, as in the long-run this proves to be a more cost effective means of reporting to IATI.



Other Tools
============

There are other IATI publishing tools available that have been developed by Third Parties. They are:

Open Aid Register
>>>>>>>>>>>>>>>>>

The Open Aid Register (see http://www.openaidregister.org/) is a New York Law School open source project funded by the Fulbright Commission and the Government of Spain. Similarly to Aidstream it is a free to use online tool that allows users to input their data which is then converted to IATI format. 



SQL-To-IATI
>>>>>>>>>>>>

The SQL-to-IATI tool generates IATI XML data from activity data stored in a SQL database. DFID use this to publish their full set of 13000 activities each month, so it supports enterprise-grade IATI. 

The core of the database is the SchemaData schema which contains a set of tables that mirror the IATI 1.03 standard in a relational database. The data held in these tables can be output as valid IATI XML files directly from a SQL function.  

A stored procedure populates the SchemaData tables through a series of transformations from source data (for example a corporate ERP). Although the stored procedure is written to deal with DFID’s specific source data, it would be a good starting point. During transformation the PublicationControl schema is used to control the data to be published to IATI, for example it contains a table to allow the exclusion of activities from publication to the IATI registry. The CodeList schema holds all of the IATI standing data (i.e. lists of valid countries, currencies and Aid Type categories), taken from the IATI codelists. 

DFID are willing to share the codebase with organisations as they seek to publish more data to the IATI standard. They would like to partner with others interested in developing this further as an open source tool for the IATI community. Contact John Adams or Ross Clements if you are interested.
