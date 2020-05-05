Forming Queries
===============

You can query the Datastore by building queries from filters. The identified data can then be output in an `XML </http://iatistandard.org/guidance/datastore/guidance/data-formats/#xml>`__, `JSON <http://iatistandard.org/guidance/datastore/guidance/data-formats/#json>`__ or `CSV <http://iatistandard.org/guidance/datastore/guidance/data-formats/#csv>`__ format depending on your needs.

Basic Query
-----------

A basic query will undertake no filtering, allowing you to access all the data in the Datastore.

Example: Query the Datastore, undertaking no filtering.

* XML: `http://datastore.iatistandard.org/api/1/access/activity.xml <http://datastore.iatistandard.org/api/1/access/activity.xml>`__
* JSON: `http://datastore.iatistandard.org/api/1/access/activity.json <http://datastore.iatistandard.org/api/1/access/activity.json>`__
* CSV: `http://datastore.iatistandard.org/api/1/access/activity.csv <http://datastore.iatistandard.org/api/1/access/activity.csv>`__

Use a Filter
------------

You can build Datastore queries by using filters. This allows you to access information about only the activities that are relevant to your needs.

Example: Query for activities that provide benefit to Uganda (UG).

* XML: `http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=UG <http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=UG>`__
* JSON: `http://datastore.iatistandard.org/api/1/access/activity.json?recipient-country=UG <http://datastore.iatistandard.org/api/1/access/activity.json?recipient-country=UG>`__
* CSV: `http://datastore.iatistandard.org/api/1/access/activity.csv?recipient-country=UG <http://datastore.iatistandard.org/api/1/access/activity.csv?recipient-country=UG>`__

The `recipient-country` filter returns activities with your specified value from the IATI `Country codelist <http://iatistandard.org/codelists/Country/>`__ – in this case, UG (Uganda).

Selecting multiple Values
-------------------------

You can request data matching multiple values for each filter by using the `|` operator. This acts as an `or`.

Example: Query for activities that provide benefit to Bangladesh (BD) **or** Honduras (HN) **or** Madagascar (MG).

* XML: `http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=BD|HN|MG <http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=BD|HN|MG>`__
* JSON: `http://datastore.iatistandard.org/api/1/access/activity.json?recipient-country=BD|HN|MG <http://datastore.iatistandard.org/api/1/access/activity.json?recipient-country=BD|HN|MG>`__
* CSV: `http://datastore.iatistandard.org/api/1/access/activity.csv?recipient-country=BD|HN|MG <http://datastore.iatistandard.org/api/1/access/activity.csv?recipient-country=BD|HN|MG>`__

Combining Filters
-----------------

You can combine multiple filters to further restrict the requested data by using the `&` operator. This acts as an `and`.

Example: Query for activities that are classified using the `DAC Sector Code <http://iatistandard.org/codelists/Sector/>`__ for Teacher Training (11130) **and** are published by the UK Department for International Development (GB-GOV-1).

* XML: `http://datastore.iatistandard.org/api/1/access/activity.xml?sector=11130&iati-identifier=GB-GOV-1 <http://datastore.iatistandard.org/api/1/access/activity.xml?sector=11130&iati-identifier=GB-GOV-1>`__
* JSON: `http://datastore.iatistandard.org/api/1/access/activity.json?sector=11130&iati-identifier=GB-GOV-1 <http://datastore.iatistandard.org/api/1/access/activity.json?sector=11130&iati-identifier=GB-GOV-1>`__
* CSV: `http://datastore.iatistandard.org/api/1/access/activity.csv?sector=11130&iati-identifier=GB-GOV-1 <http://datastore.iatistandard.org/api/1/access/activity.csv?sector=11130&iati-identifier=GB-GOV-1>`__

The `iati-identifier` filter returns activities with your specified IATI `Organisation Identifier <http://iatistandard.org/organisation-identifiers//>`__ – in this case, DFID (GB-GOV-1).

Pagination
----------

IATI has a lot of published data. The Datastore can return a lot of data for some queries.  Because of this, the Datastore returns 50 activities at a time by default. Each set of activities represent a ‘page’. This process is referred to as *pagination*.

You can use the `limit` filter to change the maximum number of returned activities, and `offset` to change which activity to start with.

Example: View 20 activities benefiting Honduras (HN), starting with the 23rd activity.

* XML: `http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=HN&limit=20&offset=23 <http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=HN&limit=20&offset=23>`__
* JSON: `http://datastore.iatistandard.org/api/1/access/activity.json?recipient-country=HN&limit=20&offset=23 <http://datastore.iatistandard.org/api/1/access/activity.json?recipient-country=HN&limit=20&offset=23>`__
* CSV: `http://datastore.iatistandard.org/api/1/access/activity.csv?recipient-country=HN&limit=20&offset=23 <http://datastore.iatistandard.org/api/1/access/activity.csv?recipient-country=HN&limit=20&offset=23>`__

The Datastore will return a 404 error page when you specify an `offset` greater than the number of returned activities.

You can return all activities, no matter how many there are, by adding `&stream=True` to your filter. This will override any other pagination options.

More Information
----------------

For in-depth detail of all the available filters, see the `Reference <http://iatistandard.org/guidance/datastore/reference/data-api/>`__.
