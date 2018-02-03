Data API
========

The following filters are available, which enable you to construct a query for the data that you are looking for.

Available filters
~~~~~~~~~~~~~~~~~

iati-identifier
```````````````

Returns activities matching your specified `IATI Identifier <http://iatistandard.org/activity-standard/iati-identifier/>`__ value.  In practice, no more than one activity should be returned as each activity should contain a unique `IATI Identifier <http://iatistandard.org/activity-standard/iati-identifier/>`__ value.

Parameters:
  iati-identifier: String denoting an individual IATI activity ID

Example API call:
    `iati-identifier=NL-KVK-41177206-C-002350 <http://datastore.iatistandard.org/api/1/access/activity.xml?iati-identifier=NL-KVK-41177206-C-002350>`__


recipient-country
`````````````````

Returns activities where the `recipient-country <http://iatistandard.org/activity-standard/iati-activities/iati-activity/recipient-country/>`__ element has a @code attribute value that matches your specified ISO country code.

Parameters:
  recipient-country: 2-digit ISO country code that appears on the `country codelist <http://iatistandard.org/codelists/Country/>`__

Example API call:
    `recipient-country=SS <http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=SS>`__


recipient-region
````````````````

Returns activities where the `recipient-region <http://iatistandard.org/activity-standard/iati-activities/iati-activity/recipient-region/>`__ element has a @code attribute value that matches your specified region code.

Parameters:
    recipient-region: A region code that appears in a recipient region `@code attribute <http://iatistandard.org/202/activity-standard/iati-activities/iati-activity/recipient-region/#attributes>`__

Example API call:
    `recipient-region=298 <http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-region=298>`__


reporting-org
`````````````

Returns activities where the `reporting-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/reporting-org/>`__ element has a @ref attribute value that matches your specified `Organisation identifier <http://iatistandard.org/organisation-identifiers/>`__ string.

Parameters:
    reporting-org: Organisation identifier string.

Example API call:
    `reporting-org=NL-KVK-41177206 <http://datastore.iatistandard.org/api/1/access/activity.xml?reporting-org=NL-KVK-41177206>`__


reporting-org.type
``````````````````

Returns activities where the `reporting-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/reporting-org/>`__ element has a @type attribute value that matches your specified value.

Parameters:
    recipient-org.type: 2-digit value that appears on the `organisation type codelist<http://iatistandard.org/codelists/OrganisationType/>`__

Example API call:
    `reporting-org.type=10 <http://datastore.iatistandard.org/api/1/access/activity.xml?reporting-org.type=10>`__


sector
``````

Returns activities where the `sector <http://iatistandard.org/codelists/Sector/>`__ element has a @code attribute value that matches your specified sector code.

Parameters:
    sector: A sector code that appears on a sector's `@code attribute <http://iatistandard.org/202/activity-standard/iati-activities/iati-activity/sector/#attributes>`__

Example API call:
    `sector=11110 <http://datastore.iatistandard.org/api/1/access/activity.xml?sector=11110>`__


policy-marker
`````````````

Returns activities where a `policy-marker <http://iatistandard.org/activity-standard/iati-activities/iati-activity/policy-marker/>`__ element has a @code attribute value that matches your specified policy-marker value.

Parameters:
    policy-marker: 1-digit value that appears on the `policy marker codelist<http://iatistandard.org/codelists/PolicyMarker/>`__

Example API call:
    `policy-marker=1 <http://datastore.iatistandard.org/api/1/access/activity.xml?policy-marker=1>`__


participating-org
``````````````````

Returns activities where the `participating-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/reporting-org/>`__ element has a @ref attribute value that matches your specified participating-org identification string.

Parameters:
    participating-org: Identification string for the organisation who is participating

Example API call:
    `participating-org=NL-KVK-41177206 <http://datastore.iatistandard.org/api/1/access/activity.xml?participating-org=NL-KVK-41177206>`__


participating-org.role
``````````````````````

Returns activities where the `participating-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/participating-org/>`__ element has a @role attribute value that matches your specified value.

Parameters:
    participating-org.role: 1-digit value that appears on the organisation role codelist

Example API call:
    `participating-org.role=1 <http://datastore.iatistandard.org/api/1/access/activity.xml?participating-org.role=1>`__


related-activity
````````````````

Returns activities where the `related-activity <http://iatistandard.org/activity-standard/iati-activities/iati-activity/related-activity/>`__ element has a @ref attribute value that matches your specified `IATI activity identifier <http://iatistandard.org/activity-standard/overview/iati-identifier/>`__ string.

Parameters:
    related-activity: String denoting an `IATI activity identifier <http://iatistandard.org/activity-standard/overview/iati-identifier/>`__

Example API call:
    `related-activity=US-7-GB-10-e76c5505 <http://datastore.iatistandard.org/api/1/access/activity.xml?related-activity=US-7-GB-10-e76c5505>`__


transaction
```````````

Returns activities containing at least one `transaction element <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/>`__ where the @ref attribute matches your given string.

Parameters:
    transaction: String denoting a `transaction @ref attribute <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/#attributes>`__

Example API call:
    `transaction=15458 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction=15458>`__


transaction_provider-org
````````````````````````

Returns activities containing at least one `transaction element <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/>`__ where the provider-org element has a @ref attribute value that matches your specified organisation identifier string.

Parameters:
    transaction_provider-org: `Organisation identifier string <http://iatistandard.org/organisation-identifiers/>`__ for the organisation issuing who provided transaction funds

Example API call:
    `transaction_provider-org=GB-1 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction_provider-org=GB-1>`__


transaction_provider-org.provider-activity-id
`````````````````````````````````````````````

Returns activities containing at least one `transaction element <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/>`__ where the `provider-activity-id <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/provider-org/#attributes>`__ element matches your specified `IATI activity identifier <http://iatistandard.org/activity-standard/overview/iati-identifier/>`__ string.

Parameters:
    transaction_provider-org.provider-activity-id: String denoting an `IATI activity identifier <http://iatistandard.org/activity-standard/overview/iati-identifier/>`__

Example API call:
    `transaction_provider-org.provider-activity-id=GB-1-202505 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction_provider-org.provider-activity-id=GB-1-202505>`__


transaction_receiver-org
````````````````````````

Returns activities containing at least one `transaction element <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/>`__ where funds have been transferred to an organisation with your specified `Organisation identifier <http://iatistandard.org/organisation-identifiers/>`__ string.

Parameters:
    transaction_receiver-org: `Organisation identifier string <http://iatistandard.org/organisation-identifiers/>`__ for the organisation issuing who received transaction funds

Example API call:
    `transaction_receiver-org=GB-CHC-1108464 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction_receiver-org=GB-CHC-1108464>`__


transaction_receiver-org.receiver-activity-id
`````````````````````````````````````````````

Returns activities containing at least one `transaction element <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/>`__ where the `receiver-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/receiver-org/#attributes>`__
element has an @receiver-activity-id attribute that matches your specified `IATI activity identifier string <http://iatistandard.org/activity-standard/overview/iati-identifier/>`__.

Parameters:
    transaction_receiver-org.receiver-activity-id: String denoting an `IATI activity identifier <http://iatistandard.org/activity-standard/overview/iati-identifier/>`__

Example API call:
    `transaction_receiver-org.receiver-activity-id=GB-CHC-1099776-B8 <http://datastore.iatistandard.org/api/1/access/activity.xml?transaction_receiver-org.receiver-activity-id=GB-CHC-1099776-B8>`__


start-date
``````````

Returns activities where the value of an `@activity-date attribute <http://iatistandard.org/activity-standard/iati-activities/iati-activity/activity-date/#attributes>`__ within an `@activity-date <http://iatistandard.org/activity-standard/iati-activities/iati-activity/activity-date>`__ element (with `@type <http://iatistandard.org/activity-standard/iati-activities/iati-activity/activity-date/#activity-date>`__ equivalent to start-planned or start-actual) is chronologically before or after your specified query value.

To return activities before your specified date, use ‘start-date__lt’
To return activities after your specified date use ‘start-date__gt’

Parameters:
    start-date: ISO format date (YYYY-MM-DD).

Example API calls:
    `start-date__lt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?start-date__lt=2015-01-01>`__
    `start-date__gt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?start-date__gt=2015-01-01>`__


end-date
````````

Returns activities where the value of an `@activity-date attribute <http://iatistandard.org/activity-standard/iati-activities/iati-activity/activity-date/#attributes>`__ within an `@activity-date <http://iatistandard.org/activity-standard/iati-activities/iati-activity/activity-date>`__ element (with `@type <http://iatistandard.org/activity-standard/iati-activities/iati-activity/activity-date/#activity-date>`__ equivalent to end-planned or end-actual) is chronologically before or after your specified query value.

To return activities before your specified date, use ‘end-date__lt’
To return activities after your specified date use ‘end-date__gt’

Parameters:
    end-date: ISO format date (YYYY-MM-DD).

Example API calls:
    `end-date__lt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?start-date__lt=2015-01-01>`__
    `end-date__gt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?start-date__gt=2015-01-01>`__


.. _`last-change`:

last-change
```````````

Returns activities where the observed last change the of an activity is chronologically before or after your specified query value. This information is provided by Datastore update processes, rather than the actual IATI data.

To return activities before your specified date use ‘last-change__lt’
To return activities after your specified date use ‘last-change__gt’

Parameters:
    last-change: ISO format date (YYYY-MM-DD).

Example API calls:
    `last-change__lt=2009-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?last-change__lt=2009-01-01>`__
    `last-change__gt=2009-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?last-change__gt=2009-01-01>`__


.. _`last-updated-datetime`:

last-updated-datetime
`````````````````````

Returns activities where the @last-updated-datetime attribute of an activity is chronologically before or after your specified query value.

To return activities before your specified date use ‘last-updated-datetime__lt’
To return activities after your specified date use ‘last-updated-datetime__gt’

Parameters:
    last-updated-datetime: ISO format date (YYYY-MM-DD).

Example API calls:
    `last-updated-datetime__lt=2015-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?last-updated-datetime__lt=2015-01-01>`__
    `last-updated-datetime__gt=2010-01-01 <http://datastore.iatistandard.org/api/1/access/activity.xml?last-updated-datetime__gt=2010-01-01>`__


registry-dataset
````````````````

Returns activities contained within your specified registry dataset.

Parameters:
    registry-dataset: string name of the specified registry dataset

Example API call:
    `registry-dataset=dfid-af <http://datastore.iatistandard.org/api/1/access/activity.xml?registry-dataset=dfid-af>`__
