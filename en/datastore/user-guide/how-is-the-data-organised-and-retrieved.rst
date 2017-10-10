How is the data organised and retrieved?
========================================

Activities
----------

Each activity reported in IATI-XML format is stored as a unique record in the Datastore. In IATI terminology an “activity” can be a project, programme, grant or any other user-defined unit of aid. The Datastore uses the <iati-identifier> element as the key to defining a unique record.

Transactions
------------

As a single activity usually contains multiple financial transactions (incoming funds, disbursements, expenditures, etc) these are stored separately such that each transaction is a separate record, linked to the parent activity through the <iati-identifier>. This structure makes it possible to generate spreadsheet output of transaction details with one row per transaction rather than just one row per activity.

Budgets
-------

Forward looking budgets are also stored and accessed in a manner similar to transactions.

Results and geocoding
---------------------

Easy-to-use output of results and location data are not yet available in CSV format. This data is available to developers through JSON and XML outputs.

Original XML data
-----------------

When data is loaded into the Datastore it is deconstructed from its original XML format and saved into a database structure. During this process data may be subjected to a number of cleaning and formatting processes to enhance its usefulness. To ensure its integrity the Datastore also keeps a copy of the original XML for each individual activity.
