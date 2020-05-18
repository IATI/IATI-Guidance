Error API
=========

The error API returns data about any problems that the Datastore encountered while attempting to process datasets. The data can be retrieved in either JSON or plain text format.

The following information is provided:

* **datestamp**: When the error occurred.
* **resource_url**: The URL of the errored resource/dataset.
* **msg**: What error message was returned.
* **traceback**: A detailed traceback of the error. Useful if you are a developer. Please include this if you need to report any errors to us.
* **logger**: The logger that reported the error.

api/1/error/dataset
```````````````````

Retrieves an unordered list of all datasets which encountered errors when parsed by the Datastore.

A plain text format is also available by appending `.log`: `http://datastore.iatistandard.org/api/1/error/dataset.log <http://datastore.iatistandard.org/api/1/error/dataset.log>`__

api/1/error/dataset/<dataset-id>
````````````````````````````````

Retrieves detailed information about the error encountered with your specified dataset.

A plain text format is also available but appending `.log` before `/dataset`, i.e. `api/1/error/dataset.log/<dataset-id>`.
