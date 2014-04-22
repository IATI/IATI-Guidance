1.04 Changes
============

Changes / Additions to IATI Standard for version 1.04

Schema Changes
--------------

A full diff of all schema changes in 1.04 can be found in github at https://github.com/IATI/IATI-Schemas/compare/version-1.03...version-1.04#files_bucket

Activities schema
~~~~~~~~~~~~~~~~~

- Added :doc:`reporting-org/@secondary-reporter </activities-standard/iati-activities/iati-activity/reporting-org>` attribute

- Made a number of changes to the :doc:`/activities-standard/iati-activities/iati-activity/location` element

  * added ``location/@ref`` attribute
  * added :doc:`location/location-reach </activities-standard/iati-activities/iati-activity/location/location-reach>` element
  * added :doc:`location/location-id </activities-standard/iati-activities/iati-activity/location/location-id>` element
  * added :doc:`location/activity-description </activities-standard/iati-activities/iati-activity/location/activity-description>` element
  * :doc:`location/administrative </activities-standard/iati-activities/iati-activity/location/administrative>` gets new attributes:  ``@level``, ``@vocabulary``, ``@code``, ``@xml:lang``
  * :doc:`location/administrative </activities-standard/iati-activities/iati-activity/location/administrative>` has the following attributes deprecated: ``@country``, ``@adm1``, ``@adm2``
  * added :doc:`location/point </activities-standard/iati-activities/iati-activity/location/point>` element
  * added :doc:`location/exactness </activities-standard/iati-activities/iati-activity/location/exactness>` element
  * added :doc:`location/location-class </activities-standard/iati-activities/iati-activity/location/location-class>` element
  * added :doc:`location/feature-designation </activities-standard/iati-activities/iati-activity/location/feature-designation>` element
  * deprecated :doc:`location/gazetteer-entry </activities-standard/iati-activities/iati-activity/location/gazetteer-entry>` element
  * deprecated :doc:`location/coordinates </activities-standard/iati-activities/iati-activity/location/coordinates>` element
  * deprecated :doc:`location/location-type </activities-standard/iati-activities/iati-activity/location/location-type>` element

- Some documentation has been altered slightly

- The order that some elements are listed has changed, as this order is now used to populate the website (`commit <https://github.com/IATI/IATI-Schemas/commit/853dc481802817f1add7c7993feae5cfe08f2c06>`__)

Codelist Changes
----------------

In 1.04 the idea of Embedded and Non-Embedded codelists was introduced.

A `codelist mapping file <https://github.com/IATI/IATI-Codelists/blob/version-1.04/mapping.xml>`__ describing the mapping between codelists and xml elements, was introduced. (`discussion <http://support.iatistandard.org/entries/27805388-Mapping-between-codelists-and-schemas>`__)

New Codelists
~~~~~~~~~~~~~

Embedded:

- :doc:`/codelists/GeographicExactness`
- :doc:`/codelists/GeographicLocationClass`
- :doc:`/codelists/GeographicLocationReach`
- :doc:`/codelists/GeographicVocabulary`

Non-Embedded:

- :doc:`/codelists/OrganisationRegistrationAgency` (was previously a Google Doc)

Updated Codelists
~~~~~~~~~~~~~~~~~

Embedded:

- Added ``9`` (Other) to :doc:`/codelists/ResultType` (`discussion <http://support.iatistandard.org/entries/24090113-Suggestion-Add-other-or-undefined-to-Result-type-codelist>`__)
- Added ``NACE`` to :doc:`/codelists/Vocabulary` (`discussion <http://support.iatistandard.org/entries/29678047-Add-NACE-Codes-as-a-Vocabulary-for-Sector?page=1#post_25391443>`__)
- The categories of :doc:`/codelists/BudgetIdentifierSector` have been described differently. No codes have changed.
- The "Agency Level" (``B``) category of :doc:`/codelists/DocumentCategory` has been renamed to "Organisation Level" for consitency. (`issue <https://github.com/IATI/IATI-Codelists/issues/28>`__)

Non-Embedded:

- :doc:`/codelists/FileFormat` updated to include all IANA Media Types. Note that it no longer has names corresponding to the codes, as the source codelist does not have this. (`discussion <http://support.iatistandard.org/entries/22915207-Additions-to-File-Format-code-list>`__)
- :doc:`/codelists/LocationType` updated to include all US NGA Feature Designation Codes
