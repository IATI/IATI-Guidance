Geography - sub-national locations
==================================

The sub-national location/s of an activity can be described in a number of ways. The primary way is through geographic coordinates. This allows data users to locate on a map all the activities happening in a particular area and build up a picture of what activities are happening where (e.g. the distribution of sustainable farming programmes). In addition, descriptions can be added, such as the name of a district and any features of the location e.g. health centre, village, administrative area. Publishing reliable location data is often very helpful for data users.

The name of an activity's location can also be included in the description element of the activity. This allows data users to find relevant activities when doing a free word search for specific location names.

Details that could link to the identification of groups and compromise the safety of people should not be added. It is the responsibility of the publishing organisation to ensure that the data they publish is safe.

How to find an activity’s ‘location’
------------------------------------

It is recommended that the `location <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/>`__ element is only used for an activity if some details are known about where in a country the activity will be taking place, and that these details are safe to add. The activity `scope <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/activity-scope/>`__ element should be used to detail what kind of sub-national location data can be included:

-  5 sub-national: multi-first-level administrative areas

-  6 sub-national: single first-level administrative area

-  7 sub-national: single second-level administrative area

-  8 Single location

A number of activities will not be based in a specific location, or it may not be known where within a country the many activities being contracted will take place. Security concerns may also prevent location data from being published, or may limit what location description can be provided. The location data provided should be aligned with the data provided in the activity’s scope element, e.g. the specific location, implementing partner’s office, central feature in an administrative area or a central coordinate for the region.

It is then for the publisher to decide how much information and context to provide about the activity’s location using the other location elements and attributes available.

If you don’t have an internal way of specifying or finding coordinates for a specific location, the website `Latlong.net <https://www.latlong.net/>`__ provides the central point for chosen areas. For example, users can search for the name of a district of administrative area and the coordinates for the central point will be provided. Or, it is possible to search for the coordinates to find where the activity is located.

Please note that, in IATI, a user should be able to trace a donor’s activity, all the way down to the multiple implementing organisations carrying out the work. It is expected that more specific location details can be added by organisations implementing the activities, rather than their funders.

How to find an activity’s coordinates
-------------------------------------

Coordinates are published using the `point <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/point/>`__ and `pos <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/point/pos/>`__ elements. The point element is always: <point srsName="http://www.opengis.net/def/crs/EPSG/0/4326">

The pos element then contains the latitude coordinate (the first number), followed by the longitude coordinate (the second number) e.g. -46.7733 167.6321.

Note that coordinates can refer to an ‘exact’ or an ‘approximate’ location. This should be specified using the location `exactness <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/exactness/>`__ element.

If you don’t already have a way to find the coordinates for an activity, there are some online platforms to help, e.g. `Google Maps <https://www.google.com/maps/>`__ and `Latlong.net <https://www.latlong.net/>`__. To find the coordinates for an activity on Google Maps, right-click over the location of the activity and select ‘what’s here?’. The coordinates will then be presented. Alternatively, type in the coordinates and the location of the activity will be pinpointed on the map.

Recommended information to be published within the location element
-------------------------------------------------------------------

Please note:

-  The location element should only be used when sub-national location data is known.

-  Location data should only be added when it is safe to do so. It is the publishing organisation’s responsibility to ensure that the data it publishes is safe.

-  Due to security considerations, some publishing organisations may decide not to include location data. They may even exclude a project from their data entirely (see `IATI’s Exclusion Policy Guidelines <https://iatistandard.org/en/guidance/standard-overview/preparing-your-organisation-data-publication/information-and-data-you-cant-publish-exclusions/>`__).

-  If required, location data can display a sub-national region with a central coordinate rather than an exact location.

-  Multiple locations can be given for an individual activity. However, please note: adding multiple locations covering a large area obstructs data use.

-  The location/s provided should relate to either the specific place or area where the activity is happening, or where the intended beneficiaries are located. This should be specified using the `location-reach <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/location-reach/>`__ element.

-  Each location should be published in a separate location element.

-  The town or region’s name, if known, should be published in the location name element.

Technical guidance summary
--------------------------

The table below shows some of the information that should be included in location elements. The full table of all the location elements that can be published is :doc:`here <sub-national-locations-all>`.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `location <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/>`__
     - Details the geographic locations in which the activity is taking place.
     -
     - The @ref attribute should be included; this is an internal reference for each location element.

       This can be used to link one of the activity’s `results <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/>`__ to a defined location.

   * - `location-reach <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/location-reach/>`__
     - Specifies whether the location is where the activity is happening or where the intended beneficiaries live.
     - This can only be published once.

       The value must be on the `geographic location reach <http://reference.iatistandard.org/codelists/GeographicLocationReach/>`__ codelist.
     -

   * - `name <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/name/>`__
     - The name of the location.
     - This can only be published once.
     - The name can be repeated in multiple languages.

   * - `description <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/description/>`__
     - A description of the location.
     - This can only be published once.
     - The description can be repeated in multiple languages.

   * - `point <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/point/>`__ and `pos <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/point/pos/>`__
     - This holds the geo-coordinates for the location, in the format of latitude and longitude coordinates.
     - The point element must contain the @srsName attribute with the value:

       http://www.opengis.net/def/crs/EPSG/0/4326"
     - The latitude and longitude coordinates are published within the pos element.

   * - `exactness <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/location/exactness/>`__
     - Specifies whether the location provided is exact or approximate.
     - This value must be on the `geographic exactness <http://reference.iatistandard.org/codelists/GeographicExactness/>`__ codelist.
     -

Activity geography
------------------
Activities can also contain countries and regions in which they are happening. For further details see:
  - :doc:`Activity geography <activity-geography>`
  - :doc:`Countries and regions <countries-regions>`

.. meta::
  :title: Geography - sub-national locations
  :description: The sub-national location/s of an activity can be described in a number of ways. The primary way is through geographic coordinates.
  :guidance_type: activity
