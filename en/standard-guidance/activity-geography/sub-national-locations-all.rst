Geography - sub-national locations (all elements)
=================================================

This table lists all elements that can be included in the location element. It includes all the recommended elements, as outlined on the `geography - sub-national locations <https://drive.google.com/open?id=1GYRE3FBhf2W4wkpTzbgKFtAWYSLG4Jw8>`__ page, plus further elements that can be used to build a comprehensive picture of an activity's location, if known.

Technical guidance summary
--------------------------

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `location <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/>`__
     - Details the geographical locations in which the activity is taking place.
     -
     - The @ref attribute should be included; this is an internal reference for each location element.

       This can be used to link one of the activity’s `results <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/>`__ to a defined location.

   * - `location-reach <http://reference.iatistandard.org/203/activity-standard/iati-activities/iati-activity/location/location-reach/>`__
     - Specifies whether the location is where the activity is happening or where the intended beneficiaries live.
     - This can only be published once.

       The value must be on the `geographic location reach <http://reference.iatistandard.org/codelists/GeographicLocationReach/>`__ codelist.
     -

   * - `location-id <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/location-id/>`__
     - A unique code describing the location according to a recognised gazetteer or repository of administrative boundaries.
     - The must come from one of the lists on the `geographic vocabulary <http://reference.iatistandard.org/codelists/GeographicVocabulary/>`__ codelist.
     - Administrative areas should be published here only if the location being defined is the administrative area itself.

       For describing the administrative area/s within which a more specific location falls, the location/administrative element should be used.

   * - `name <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/name/>`__
     - The name of the location
     - This can only be published once.
     - The name can be repeated in multiple languages.

   * - `description <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/description/>`__
     - A description of the location
     - This can only be published once.
     - The description can be repeated in multiple languages.

   * - `activity-description <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/activity-description/>`__
     - A description that qualifies the activity taking place at the location.
     - This can only be published once.
     - This should be used when the activity has multiple locations; can be used to specify what activity is happening at each location.

       This should not duplicate information provided elsewhere.

   * - `administrative <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/administrative/>`__
     - A unique code describing the location according to an administrative boundary repository.
     - This must come from one of the lists on the `geographic vocabulary <http://reference.iatistandard.org/codelists/GeographicVocabulary/>`__ codelist.
     -

   * - `point <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/point/>`__ and `pos <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/point/pos/>`__
     - This holds the geo-coordinates for the location, in the format of latitude and longitude.
     - The point element must contain the @srsName attribute with the value:

       http://www.opengis.net/def/crs/EPSG/0/4326"
     - The latitude and longitude coordinates are published within the pos element.

   * - `exactness <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/exactness/>`__
     - Specifies whether the location provided is exact or approximate.
     - This value must be on the `geographic exactness <http://reference.iatistandard.org/codelists/GeographicExactness/>`__ codelist.
     -

   * - `location-class <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/location-class/>`__
     - Specifies the form of the location e.g. populated place (town, farm), or topographical feature (mountain, river).
     - This value must be on the `geographic location class <http://reference.iatistandard.org/codelists/GeographicLocationClass/>`__ codelist.
     -

   * - `feature-designation <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/feature-designation/>`__
     - This adds more detail to the type of location (e.g. beach, well or college).
     - This value must be on the `location type <http://reference.iatistandard.org/codelists/LocationType/>`__ codelist.
     -
