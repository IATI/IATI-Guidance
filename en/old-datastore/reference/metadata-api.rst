Metadata API
============

The metadata API returns data about the datasets that are contained within the Datastore in JSON format.  You can access this data in a number of ways:

/api/1/about/dataset
````````````````````

Returns the list of dataset IDs that are used to build the Datastore. Dataset IDs are based on their name in the `IATI Registry <https://iatiregistry.org/dataset>`__.

Example return values:

.. code-block:: json

	{
	    "datasets": [
	        "open_university-activities",
	        "aqua4all-nl_2",
	        "aqua4all-nl_3",
	        "aqua4all-nl_4",
	        ...
	    ]
	}

/api/1/about/dataset/<dataset-id>
`````````````````````````````````

Returns specific details for a given dataset ID.

Contains datetimes for the last modification, last fetch and parse dates for the given dataset. The source dataset URL and the number of IATI activities contained within the dataset is also returned.

* **dataset**: The ID of the dataset.
* **last_modified**: The timestamp that the dataset was updated in the IATI Registry.
* **num_resources**: The length of the resources array.
* **resources**: A list of metadata objects for every resource returned.
	* **last_fetch**: The timestamp that the last fetch was attempted.
	* **last_parsed**: The timestamp that the resource was last successfully parsed.
	* **last_status_code**: The HTTP status code for the last fetch.
	* **last_successful_fetch**: The latest timestamp that the Datastore successfully fetched the resource.
	* **num_of_activities**: The number of activities the Datastore has successfully parsed and stored for this resource.
	* **url**: The URL that the Datastore used to fetch the resource.


Example return values:

.. code-block:: json

	{
	    "dataset": "open_university-activities",
	    "last_modified": "2017-10-09T13:55:47.123143",
	    "num_resources": 1,
	    "resources": [
	        {
	            "last_fetch": "2017-10-10T04:27:14.196223",
	            "last_parsed": "2017-10-10T04:30:30.892844",
	            "last_status_code": 200,
	            "last_successful_fetch": "2017-10-10T04:27:14.196320",
	            "num_of_activities": 2,
	            "url": "https://aidstream.org/files/xml/open_university-activities.xml"
	        }
	    ]
	}
