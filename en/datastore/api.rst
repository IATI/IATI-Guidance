Datastore API
=============

.. contents::

.. toctree::
  :glob:

Available data
--------------

IATI activity data is available in the following formats:

Technical formats
~~~~~~~~~~~~~~~~~
-  XML - using endpoint: `/api/1/access/activity.xml <http://datastore.iatistandard.org/api/1/access/activity.xml>`__
-  JSON - using endpoint: `/api/1/access/activity.json <http://datastore.iatistandard.org/api/1/access/activity.json>`__

CSV formats
~~~~~~~~~~~
-  List of activities `/api/1/access/activity.csv <http://datastore.iatistandard.org/api/1/access/activity.csv>`__
-  Activities by sector `/api/1/access/activity/by_sector.csv <http://datastore.iatistandard.org/api/1/access/activity/by_sector.csv>`__
-  Activities by country `/api/1/access/activity/by_country.csv <http://datastore.iatistandard.org/api/1/access/activity/by_country.csv>`__
-  List of transactions `/api/1/access/transaction.csv <http://datastore.iatistandard.org/api/1/access/transaction.csv>`__
-  Transactions by sector `/api/1/access/transaction/by_sector.csv <http://datastore.iatistandard.org/api/1/access/transaction/by_sector.csv>`__
-  Transactions by country `/api/1/access/transaction/by_country.csv <http://datastore.iatistandard.org/api/1/access/transaction/by_country.csv>`__
-  List of budgets `/api/1/access/budget.csv <http://datastore.iatistandard.org/api/1/access/budget.csv>`__
-  Budgets by sector `/api/1/access/budget/by_sector.csv <http://datastore.iatistandard.org/api/1/access/budget/by_sector.csv>`__
-  Budgets by country `/api/1/access/budget/by_country.csv <http://datastore.iatistandard.org/api/1/access/budget/by_country.csv>`__



Filtering
---------

The following filters are available, which enable you to construct a query for the data that you are looking for.

Available filters
~~~~~~~~~~~~~~~~~

iati-identifier
```````````````

Returns activities matching the specified `IATI Identifier <http://iatistandard.org/activity-standard/iati-identifier/>`__ element.  In practice this should return one activity, as each activity should contain a `IATI Identifier <http://iatistandard.org/activity-standard/iati-identifier/>`__ value.

Parameters:
    @iati-identifier: String denoting an individual IATI activity

Example API call:
    `/api/1/access/activity.xml?iati-identifier=NL-KVK-41177206-C-002350 <http://datastore.iatistandard.org/api/1/access/activity.xml?iati-identifier=NL-KVK-41177206-C-002350>`__


recipient-country
`````````````````

Returns activities where the country contained within a `recipient-country <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/recipient-country/>`__ element matches a specified ISO country code.

Parameters:
    @recipient-country: 2-digit ISO country code which appears on the `country codelist <http://iatistandard.org/201/codelists/Country/>`__

Example API call:
    `/api/1/access/activity.xml?recipient-country=SS <http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=SS>`__


recipient-region
````````````````

Returns activities where the contained within with a `recipient-region <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/recipient-region/>`__ element matches a specified DAC region code.

Parameters:
    @recipient-region: 3-digit DAC region code which appears on the `region codelist <http://iatistandard.org/201/codelists/Region/>`__

Example API call:
    `/api/1/access/activity.xml?recipient-region=298 <http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-region=298>`__


reporting-org
`````````````

Returns activities where the value contained within a `reporting-org <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/reporting-org/>`__ element matches your specified `Organisation identifier <http://iatistandard.org/201/organisation-identifiers/>`__ string.

Parameters:
    @reporting-org: Organisation identifier string.

Example API call:
    `/api/1/access/activity.xml?reporting-org=NL-KVK-41177206 <http://datastore.iatistandard.org/api/1/access/activity.xml?reporting-org=NL-KVK-41177206>`__


reporting-org.type
``````````````````

Returns activities where the value contained within a `reporting-org <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/reporting-org/>`__ @type attribute matches your specified value.

Parameters:
    @recipient-org.type: 2-digit value which appears on the `organisation type codelist<http://iatistandard.org/201/codelists/OrganisationType/>`__

Example API call:
    `/api/1/access/activity.xml?reporting-org.type=10 </api/1/access/activity.xml?reporting-org.type=10>`__


sector
``````

Returns activities where the value contained within a `sector <http://iatistandard.org/201/codelists/Sector/>`__ element matches a specified DAC sector code.

Parameters:
    @sector: 5-digit DAC sector code which appears on the `sector codelist <http://iatistandard.org/201/codelists/Sector/>`__

Example API call:
    `/api/1/access/activity.xml?sector=11110 <http://datastore.iatistandard.org/api/1/access/activity.xml?sector=11110>`__


policy-marker
`````````````

Returns activities containing a `policy-marker <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/policy-marker/>`__ element which matches a your specified policy-marker value.

Parameters:
    @policy-marker: 1-digit value which appears on the `policy marker codelist<http://iatistandard.org/201/codelists/PolicyMarker/>`__

Example API call:
    `/api/1/access/activity.xml?policy-marker=1 <http://datastore.iatistandard.org/api/1/access/activity.xml?policy-marker=1>`__


participating-org
``````````````````

Returns activities where the the value contained within the `participating-org <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/reporting-org/>`__ element matches your specified participating-org identification string.

Parameters:
    @participating-org: Identification string for the organisation who is participating

Example API call:
    `/api/1/access/activity.xml?participating-org=NL-KVK-41177206 <http://datastore.iatistandard.org/api/1/access/activity.xml?participating-org=NL-KVK-41177206>`__


participating-org.role
``````````````````````

Returns activities where the value contained within the `participating-org <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/participating-org/>`__ @role attribute matches your specified value.

Parameters:
    @participating-org.role: 1-digit value which appears on the organisation role codelist

Example API call:
    `/api/1/access/activity.xml?participating-org.role=1 <http://datastore.iatistandard.org/api/1/access/activity.xml?participating-org.role=1>`__


related-activity
````````````````

Returns activities where the value contained within at least one `related-activity <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/related-activity/>`__ element within an activity matches a specified `IATI activity identifier <http://iatistandard.org/201/activity-standard/overview/iati-identifier/>`__ string.

Parameters:
    @related-activity: String denoting an `IATI activity identifier <http://iatistandard.org/201/activity-standard/overview/iati-identifier/>`__

Example API call:
    `/api/1/access/activity.xml?related-activity=US-7-GB-10-e76c5505 <http://datastore.iatistandard.org/api/1/access/activity.xml?related-activity=US-7-GB-10-e76c5505>`__


transaction
```````````

Returns activities containing at least one `transaction element <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/transaction/>`__ where the @ref attribute matches your given string.

Parameters:
    @transaction: String denoting an `transaction @ref attribute <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/transaction/#attributes>`__

Example API call:
    `/api/1/access/activity.xml?transaction=15458 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction=15458>`__


transaction_provider-org
````````````````````````

Returns activities containing at least one `transaction element <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/transaction/>`__ where the provider-org element matches your specified organisation identifier string.

Parameters:
    @transaction_provider-org: `Organisation identifier string <http://iatistandard.org/201/organisation-identifiers/>`__ for the organisation issuing who provided transaction funds

Example API call:
    `/api/1/access/activity.xml?transaction_provider-org=GB-1 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction_provider-org=GB-1>`__


transaction_provider-org.provider-activity-id
`````````````````````````````````````````````

Returns activities containing at least one `transaction element <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/transaction/>`__ where the `provider-activity-id <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/transaction/provider-org/#attributes>`__ element matches a specified `IATI activity identifier <http://iatistandard.org/201/activity-standard/overview/iati-identifier/>`__ string.

Parameters:
    @transaction_provider-org.provider-activity-id: String denoting an `IATI activity identifier <http://iatistandard.org/201/activity-standard/overview/iati-identifier/>`__

Example API call:
    `/api/1/access/activity.xml?transaction_provider-org.provider-activity-id=GB-1-202505 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction_provider-org.provider-activity-id=GB-1-202505>`__


transaction_receiver-org
````````````````````````

Returns activities containing at least one `transaction element <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/transaction/>`__ where funds have been transferred to an organisation with the specified `Organisation identifier <http://iatistandard.org/201/organisation-identifiers/>`__ string.

Parameters:
    @transaction_receiver-org: `Organisation identifier string <http://iatistandard.org/201/organisation-identifiers/>`__ for the organisation issuing who received transaction funds

Example API call:
    `/api/1/access/activity.xml?transaction_receiver-org=GB-CHC-1108464 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction_receiver-org=GB-CHC-1108464>`__


transaction_receiver-org.receiver-activity-id
`````````````````````````````````````````````

Returns activities containing at least one `transaction element <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/transaction/>`__ where the `receiver-org <http://iatistandard.org/201/activity-standard/iati-activities/iati-activity/transaction/receiver-org/#attributes>`__
element has an @receiver-activity-id attribute which matches the specified `IATI activity identifier string <http://iatistandard.org/201/activity-standard/overview/iati-identifier/>`__.

Parameters:
    @transaction_receiver-org.receiver-activity-id: String denoting an `IATI activity identifier <http://iatistandard.org/201/activity-standard/overview/iati-identifier/>`__

Example API call:
    `/api/1/access/activity.xml?transaction_receiver-org.receiver-activity-id=GB-CHC-1099776-B8 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction_receiver-org.receiver-activity-id=GB-CHC-1099776-B8>`__


start-date
``````````

Returns activities where the date with in @activity-date element (with type equivalent to start-planned or start-actual) of an activity is less or greater than your specified query.

This API element has two sub-elements: to return activities less than your specified date, use start-date__lt, or to return activities less than your specified date use start-date__gt

Parameters:
    @start-date: ISO format date (YYYY-MM-DD).

Example API calls:
    `/api/1/access/activity.xml?start-date__lt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?start-date__lt=2015-01-01>`__
    `/api/1/access/activity.xml?start-date__gt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?start-date__gt=2015-01-01>`__


end-date
````````

Returns activities where the @activity-date element (with type equivalent to end-planned or end-actual) of an activity is less or greater than your specified query.

This API element has two sub-elements: to return activities less than your specified date, use end-date__lt, or to return activities less than your specified date use end-date__gt

Parameters:
    @end-date: ISO format date (YYYY-MM-DD).

Example API call:
    `/api/1/access/activity.xml?end-date__lt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?end-date__lt=2015-01-01>`__
    `/api/1/access/activity.xml?end-date__gt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?end-date__gt=2015-01-01>`__


.. _`last-change`:

last-change
```````````

Returns activities where the observed last change the of an activity is less or greater than your specified query.

This differs from the `last-updated-datetime`_. filter, as the last-date filter is based on when the Datastore process observed a change in data. The `last-updated-datetime`_. filter returns data based on the @last-updated-datetime attribute contained within the data itself.

This API element has two sub-elements: to return activities less than your specified date, use last-change__lt, or to return activities less than your specified date use last-change__gt

Parameters:
    @last-change: ISO format date (YYYY-MM-DD).

Example API calls:
    `/api/1/access/activity.xml?last-change__lt=2009-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?last-change__lt=2009-01-01>`__
    `/api/1/access/activity.xml?last-change__gt=2009-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?last-change__gt=2009-01-01>`__


.. _`last-updated-datetime`:

last-updated-datetime
`````````````````````

Returns activities where the @last-updated-datetime attribute of an activity is less or greater than your specified query.

This differs from the `last-change`_. filter, as the last-updated-datetime filter returns data based on the @last-updated-datetime attribute contained within the data itself.  The `last-change`_. filter is based on when the Datastore process observed a change in data.

This API element has two sub-elements: to return activities less than your specified date, use last-updated-datetime__lt, or to return activities less than your specified date use last-updated-datetime__gt

Parameters:
    @last-updated-datetime: ISO format date (YYYY-MM-DD).

Example API calls:
    `/api/1/access/activity.xml?last-updated-datetime__lt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?last-updated-datetime__lt=2015-01-01>`__
    `/api/1/access/activity.xml?last-updated-datetime__gt=2010-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?last-updated-datetime__gt=2010-01-01>`__


registry-dataset
````````````````

Returns activities contained within a specified registry dataset.

Parameters:
    @registry-dataset: string name of the specified registry dataset

Example API call:
    `/api/1/access/activity.xml?registry-dataset=dfid-af <http://datastore.iatistandard.org/api/1/access/activity.xml?registry-dataset=dfid-af>`__




Combining filters
~~~~~~~~~~~~~~~~~

All of the above filters can be combined using the & character.  The resulting query will return activities which match all of the specified criteria.

Example API call:
    `/api/1/access/activity.xml?reporting-org=GB-1&recipient-country=CD <http://datastore.iatistandard.org/api/1/access/activity.xml?reporting-org=GB-1&recipient-country=CD>`__
    *This would respond with all the DFID (GB-1) data for the Democratic Republic of Congo (CD).*



Complex Filtering
~~~~~~~~~~~~~~~~~

Each individual filter can be filtered for alternate values using the | character.

Example API call:
    `/api/1/access/activity.xml?reporting-org=GB-1&recipient-country=CD|UG <http://datastore.iatistandard.org/api/1/access/activity.xml?reporting-org=GB-1&recipient-country=CD%7CUG>`__
    This would return activities for DFID (GB-1) where the recipient-country is either Democratic Republic of Congo (CD) OR Uganda (UG)



Results options
----------------------

Paging through results
~~~~~~~~~~~~~~~~~~~~~~

By default, data is returned from the first result matching your API query.  Incrementing the offset parameter will return data beginning at the *nth* activity.

    `/api/1/access/activity.xml <http://datastore.iatistandard.org/api/1/access/activity.xml>`__
    *This will return all activities, beginning with the first result.*

    `/api/1/access/activity.xml?offset=20 <http://datastore.iatistandard.org/api/1/access/activity.xml?offset=20>`__
    *This will return all activities, beginning with the 20th result.*

The datastore will respond with an HTTP 404 when you have asked for the page beyond the last page.



Setting a number of maximum results
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The maximum number of results to be returned on a ‘page’ can be set using the limit parameter.

Parameters:
    @limit: Maximum number of activities to be returned

Example API call:
    `/api/1/access/activity.xml?limit=100 <http://datastore.iatistandard.org/api/1/access/activity.xml?limit=100>`__

The default behaviour is 50. Trying to fetch more than about 1000 activities with this this call is likely to result in an error.



Getting all the results at once
-------------------------------

The CSV and XML formats support returning all results at once in a ‘stream’. To request all available results, add ‘stream=True’ to your parameters.

Example API calls:
    `/api/1/access/transaction.csv?reporting-org.ref=GB-1&stream=True <http://datastore.iatistandard.org/api/1/access/transaction.csv?reporting-org.ref=GB-1&stream=True>`__
    *This will return all the DFID transactions data as CSV.*

    `/api/1/access/activity.xml?reporting-org.ref=GB-1&stream=True <http://datastore.iatistandard.org/api/1/access/activity.xml?reporting-org.ref=GB-1&stream=True>`__
    *This will return all the DFID transactions data as XML.*



Checking the Data
-----------------

General information is available on datasets contained within the datastore, as well as datasets where errors were encountered during the process of fetching and parsing. Full information on this is available on the `General API <error/#general-data>`__ and `Error API <error/#errors>`__ documentation.



Source code
-----------

The IATI Datastore is still under development. You can `browse the
source code on GitHub and report bugs on
Github <https://github.com/IATI/iati-datastore>`__ using the '`Issues <https://github.com/IATI/iati-datastore/issues>`__' features.
