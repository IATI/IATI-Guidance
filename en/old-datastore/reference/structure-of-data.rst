Structure of data
=================

Raw data results of XML and JSON queries to the Datastore API have added metadata. This lets you see information about your query.

The following information is given in the metadata for your query:

* **generated-datetime**: This shows the time the query was run.
* **ok**: This returns True when a query is successful.
* **total-count**: This shows the number of activities that match your query.
* **limit**: This shows the maximum number of activities you will see per page (see `Pagination <http://iatistandard.org/guidance/datastore/guidance/forming-queries/#pagination>`__).
* **start**: This refers to the offset value (see `Pagination <http://iatistandard.org/guidance/datastore/guidance/forming-queries/#pagination>`__).
* **iati-extra: [version]**: This shows the version of the IATI standard for each returned activity. Activities returned will not necessarily be at the same version.

XML
---

The XML data is structured in the following way:

.. code-block:: xml

	<result xmlns:iati-extra="http://datastore.iatistandard.org/ns">
	    <ok>True</ok>
	    <iati-activities generated-datetime="2017-10-10T13:45:31.218204">
	        <query>
	            <total-count>717482</total-count>
	            <start>0</start>
	            <limit>50</limit>
	        </query>
	        <iati-activity xmlns:example="http://example.com/example" iati-extra:version="2.01" last-updated-datetime="2015-11-10T10:53:36Z" xml:lang="en" default-currency="EUR">
	            <!-- …IATI ACTIVITY DATA HERE… -->
	        </iati-activity>
	       <!-- …OTHER ACTIVITIES… -->
	    </iati-activities>
	</result>


JSON
----

The JSON data is structured in the following way:


.. code-block:: json

	{
	    "iati-activities": [
	        "iati-activity": {
	            […IATI ACTIVITY DATA HERE…]
	            "iati-extra:version": "1.03"
	        },
	        […OTHER ACTIVITIES…]
	    ],
	    "limit": 50,
	    "ok": true,
	    "start": 0,
	    "total-count": 717482
	}



CSV
---

CSV data does not include metadata. It also has a very different structure to XML and JSON since it cannot directly represent nested information.

CSV files are returned as rows and columns which are structured by your selections.

There are three potential output formats:

* Activity (`http://datastore.iatistandard.org/api/1/access/activity.csv <http://datastore.iatistandard.org/api/1/access/activity.csv>`__) - each row contains a unique activity. Financial information is aggregated. Budget information is excluded. Other potentially repeating fields (such as sectors) are reported in a single cell, delimited by semi-colons.
* Transaction (`http://datastore.iatistandard.org/api/1/access/transaction.csv <http://datastore.iatistandard.org/api/1/access/transaction.csv>`__) - each row contains a unique financial transaction. The parent activity identifier and other activity-level fields are repeated for each transaction.
* Budget (`http://datastore.iatistandard.org/api/1/access/budget.csv <http://datastore.iatistandard.org/api/1/access/budget.csv>`__) - each row contains a budget-period entry. Transaction data is not included. The parent activity identifier and other activity-level fields are repeated for each budget line.

Each of these three formats may have rows expanded to allow analysis of percentage splits between `Sectors <http://iatistandard.org/activity-standard/iati-activities/iati-activity/sector/>`__ and `Countries <http://iatistandard.org/activity-standard/iati-activities/iati-activity/recipient-country/>`__.

* Sector (replace `.csv` with `/by_sector.csv`) – each `Activity <http://datastore.iatistandard.org/api/1/access/activity/by_sector.csv>`__, `Transaction <http://datastore.iatistandard.org/api/1/access/transaction/by_sector.csv>`__ or `Budget <http://datastore.iatistandard.org/api/1/access/budget/by_sector.csv>`__ row is repeated for each separate Sector reported. The corresponding percentage for the sector split is reported in a separate column.
* Country (replace `.csv` with `/by_country.csv`)  – each `Activity <http://datastore.iatistandard.org/api/1/access/activity/by_country.csv>`__, `Transaction <http://datastore.iatistandard.org/api/1/access/transaction/by_country.csv>`__ or `Budget <http://datastore.iatistandard.org/api/1/access/budget/by_country.csv>`__ row is repeated for each separate Country reported. The corresponding percentage for the sector split is reported in a separate column.
