Select a publishing tool
^^^^^^^^^^^^^^^^^^^^^^^^

There are currently three different mechanisms recommended by the IATI Secretariat to convert data into IATI- XML data files. Aidstream and the CSV Converter are recommended because they are both currently actively maintained with the involvement of the IATI Technical Support Team.



Aidstream
=========

Aidstream (http://www.aidstream.org) is an online data entry and management tool which you use by manually entering all of the relevant activity information through the use of drop-down menus and text boxes. Aidstream converts the data entered into XML and outputs both organisation and activity datafiles for publishing . The data stored in Aidstream can be added to or amended at any point. Aidstream is usually the tool of choice if you only have a small number of activities (approx < 15 - 20) to publish.

There is a whole series of instructional videos on using Aidstream. These can be found at `Aidstream On Youtube <https://www.youtube.com/channel/UCAVH1gcgJXElsj8ENC-bDQQ>`__


Bespoke (In House Applications)
===============================

Organisations with internal technical expertise and capacity may decide to generate their own mechanisms for converting their data into IATI data. This can be done by developing internal systems and processes so that data is pulled together from internal management and finance systems to create XML data. This requires technical knowledge of both XML and the organisation's internal systems in order to create a programme to achieve this. This can be done with either internal technical expertise or by bringing in consultants to develop a bespoke package.

This is normally an option often chosen by large organisations reporting a large number of activities, as in the long-run this proves to be a more cost effective means of reporting to IATI.



Other Tools
===========

There are other IATI publishing tools available that have been developed by Third Parties. They are:

Akvo RSR
>>>>>>>>

`Akvo Really Simple Reporting <http://akvo.org/products/rsr/#overview>`__ (RSR) is an online platform for reporting, monitoring, and publicly communicating international development programs. Features include management, tracking, and updating of projects from the desk or remotely, and RSR enables users to automatically push or pull data to or from the IATI registry.

More information about pricing can be found `here <http://akvo.org/products/rsr/#pricing>`__. For general enquiries, `contact Akvo <http://akvo.org/get-in-touch/>`__.



IATI Studio Publisher
>>>>>>>>>>>>>>>>>>>>>

Due for release in the 3rd quarter of 2016, `IATI Studio Publisher <https://www.iatistudio.com/>`__ allows for validated IATI publication, both on activity level and organisation level. Drafted data will be available before the user chooses to export the data to a valid XML file and the service is integrated with the IATI Studio Chart Builder and Micro-site Builder, more details of which can be `found here <https://www.iatistudio.com/features/>`__.

Core functionality is free; more information about pricing in premium packages can be found `here <https://www.iatistudio.com/membership/>`__. For general enquiries, `contact the IATI Studio team <https://www.iatistudio.com/support/>`__.



SQL-To-IATI
>>>>>>>>>>>

The `SQL-to-IATI tool <https://github.com/DFID/SQL-to-IATI-Database>`__ generates IATI XML data from activity data stored in a SQL database. DFID use this to publish their full set of 13000 activities each month, so it supports enterprise-grade IATI.

The core of the database is the IATISchema schema which contains a set of tables that mirror the IATI 2.01 standard XML schema in a relational database. The data held in these tables can be output as valid IATI XML files directly from a SQL function.

A stored procedure populates the IATISchema tables through a series of transformations from source data (for example a corporate ERP). Although the stored procedure is written to deal with DFID’s specific source data, it would be a good starting point. During transformation the PublicationControl schema is used to control the data to be published to IATI, for example it contains a table to allow the exclusion of activities from publication to the IATI registry. The CodeList schema holds all of the IATI standing data (i.e. lists of valid countries, currencies and Aid Type categories), taken from the IATI codelists.

DFID are willing to share the codebase with organisations as they seek to publish more data to the IATI standard, and the code is freely available on GitHub. They would like to partner with others interested in developing this further as an open source tool for the IATI community. Contact DFID’s Technical Transparency Team: devtracker-feedback@dfid.gov.uk if you are interested.


Comparison of Tools
===================

The table below provides a summary of the three main tool options that can be used to convert data for IATI purposes:

=================================================== =============================== ================================================================
Factor                                              Aidstream                       Bespoke
=================================================== =============================== ================================================================
Typical users:                                        Small organisations reporting   Large organisations with numerous activities
                                                      on small number of activities   to report who want to invest in own systems

Number of activities for publication: (rough guide) Up to 20	                      Over 200
Internal technical capacity required:               No                              Yes
Data entry type:                                    Manual	                        Automatic / built-in feed from internal systems
Input type:                                         Drop down menus and text boxes  Pulled from internal systems automatically
Availability of conversion type:                    Online and free	                Needs internal capacity / consultants to develop bespoke system
Knowledge of XML required:                          No	                            Yes
XML formats required:                               No                              No
                                                    (selected automatically through (converts this from internal systems)
                                                    drop down menus)
Automatic publication: to IATI Registry?            Yes                             Yes (if using Registry API)
Can files be segmented:                             Yes                             Yes
Organisation file ability:                          Yes                             Yes
Preparation required:                               Activity data available	        System development to ensure activity relevant data is pulled in
Resources required (set-up):                        Minimal – data entry            High – internal technical capacity or consultants required to
                                                                                    develop system
Resources required (ongoing management):            Minimal – ongoing data entry    Minimal – system able to run automatically
Updating activities:                                Manual	                         Automatic
User guidance / support available:                  Yes                             No
=================================================== =============================== ================================================================
