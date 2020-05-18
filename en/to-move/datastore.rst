Datastore (Alpha)
=================

The Datastore stores all activity data available on the IATI Registry, allowing you to query it all in one place. This data can be accessed in spreadsheet format, or in more technical formats through a standard interface (API). Please be aware that this product is considered to be in alpha (`see below <http://iatistandard.org/guidance/datastore/#alpha-status>`__).

.. toctree::
    :titlesonly:

    datastore/guidance
    datastore/reference

IATI Datastore CSV Query Builder
--------------------------------

You can perform many common queries using the `IATI Datastore CSV Query Builder <http://datastore.iatistandard.org/query/>`__. This tool generates a Datastore query in spreadsheet (CSV) format based on the fields that you select.

Overview
--------

The Datastore has three APIs:

* `Data API <http://iatistandard.org/guidance/datastore/reference/data-api/>`__: Allows you to make queries which can output IATI data in your chosen format (CSV, XML or JSON).
* `Metadata API <http://iatistandard.org/guidance/datastore/reference/metadata-api/>`__: Allows you to find information about datasets that are contained within the Datastore.
* `Error API <http://iatistandard.org/guidance/datastore/reference/error-api/>`__: Allows you to see information about datasets that could not be successfully imported into the Datastore.

Anyone can access the Datastore – just build a query and data will be returned.

Alpha Status
------------

Please be aware that the Datastore is in alpha. This means that it may exhibit unexpected behaviour or return unexpected results. This product is intended for user testing and feedback only and should not be considered a stable product. The Datastore is not feature complete.

Current known issues include:

* Invalid publisher data causing problems with data import
* Registry failure causing problems with data import

In the meantime, we welcome code contributions from our open source community via `GitHub <https://github.com/IATI/IATI-Datastore>`__.

Quick Start
-----------

The Data API is the most commonly used API. The following examples will get you started.

**Example 1: A simple query to return data for a given country**

This URL returns all available IATI activities in Somalia using the `recipient-country` filter:

`http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=SO <http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=SO>`__

Values for filters come from the relevant IATI codelist. In this case, `SO` is the value for Somalia on the Country codelist.

**Example 2: A more complex query**

This URL returns all available IATI activities in multiple countries using the `recipient-country` filter – in this case, Ethopia, Somalia and Kenya – reported by multiple reporting organisation types using the `reporting-org.type` filter – in this case, international, national and regional NGOs:

`http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=ET|SO|KE&reporting-org.type=21|22|23 <http://datastore.iatistandard.org/api/1/access/activity.xml?recipient-country=ET|SO|KE&reporting-org.type=21|22|23>`__

Next Steps
----------

The Datastore can do much more than is shown here.

* See the `Guidance <http://iatistandard.org/guidance/datastore/guidance/>`__ for a more detailed guide on querying the Datastore.
* For in-depth documentation, see the `Reference <http://iatistandard.org/guidance/datastore/reference/>`__.
