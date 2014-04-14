1.04 Changes
============

Changes / Additions to IATI Standard for version 1.04

Schema Changes
--------------

Activities schema
~~~~~~~~~~~~~~~~~

- added :doc:`reporting-org/@secondary-reporter </activities-standard/iati-activities/iati-activity/reporting-org>` attribute

- made a number of changes to the :doc:`/activities-standard/iati-activities/iati-activity/location` element

  * added ``location/@ref`` attribute
  * added :doc:`location/location-reach </activities-standard/iati-activities/iati-activity/location/location-reach>` element
  * added :doc:`location/location-id </activities-standard/iati-activities/iati-activity/location/location-id>` element
  * added :doc:`location/activity-description </activities-standard/iati-activities/iati-activity/location/activity-description>` element
  * :doc:`location/administrative </activities-standard/iati-activities/iati-activity/location/administrative>` gets new attributes:  `@level`, `@vocabulary`, `@code`, `@xml:lang`
  * :doc:`location/administrative </activities-standard/iati-activities/iati-activity/location/administrative>` has the following attributes deprecated: `@country`, `@adm1`, `@adm2`
  * added :doc:`location/point </activities-standard/iati-activities/iati-activity/location/point>` element
  * added :doc:`location/exactness </activities-standard/iati-activities/iati-activity/location/exactness>` element
  * added :doc:`location/location-class </activities-standard/iati-activities/iati-activity/location/location-class>` element
  * added :doc:`location/feature-designation </activities-standard/iati-activities/iati-activity/location/feature-designation>` element
  * deprecated :doc:`location/gazetteer-entry </activities-standard/iati-activities/iati-activity/location/gazetteer-entry>` element
  * deprecated :doc:`location/coordinates </activities-standard/iati-activities/iati-activity/location/coordinates>` element
  * deprecated :doc:`location/location-type </activities-standard/iati-activities/iati-activity/location/location-type>` element

- some documentation has been altered slightly

Codelist Changes
----------------

In 1.04 the idea of Embedded and Non-Embedded codelists was introduced.

A `codelist mapping file <https://github.com/IATI/IATI-Codelists/blob/version-1.04/mapping.xml>` describing the mapping between codelists and xml elements, was introduced. (`http://support.iatistandard.org/entries/27805388-Mapping-between-codelists-and-schemas <discussion>`__)

New Codelists
~~~~~~~~~~~~~

Embedded:

- :doc:`/codelists/GeographicExactness`
- :doc:`/codelists/GeographicLocationClass`
- :doc:`/codelists/GeographicLocationReach`
- :doc:`/codelists/GeographicVocabulary`

Non-Embedded:

- :doc:`/codelists/GeographicFeatureDesignation`
- :doc:`/codelists/OrganisationRegistrationAgency` (was previously a Google Doc)

Updated Codelists
~~~~~~~~~~~~~~~~~

Embedded:

- Added `9` (Other) to :doc:`/codelists/ResultType` (`discussion <http://support.iatistandard.org/entries/24090113-Suggestion-Add-other-or-undefined-to-Result-type-codelist>`__)
- Added `NACE` to :doc:`/codelists/Vocabulary` (`discussion <http://support.iatistandard.org/entries/29678047-Add-NACE-Codes-as-a-Vocabulary-for-Sector?page=1#post_25391443>`__)
- The categories of :doc:`/codelists/BudgetIdentifierSector` have been described differently. No codes have changed.

Non-Embedded:

- :doc:`/codelists/FileFormat` (`discussion <http://support.iatistandard.org/entries/22915207-Additions-to-File-Format-code-list>`__)
