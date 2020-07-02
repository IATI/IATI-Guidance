Geography - countries and regions
=================================

Each activity in IATI should specify the country (e.g. China) in which the activity is taking place, or the places that will benefit from the activity. If the country is not known, then a supra-national region or regions (e.g. East Asia) must be added.

An activity may cover one or more countries and regions. There are some rules about how multiple countries and regions need to be added to an activity. Having one country per activity provides more disaggregated information, which is helpful for data users. If a country is known for 100% of the activity, then the corresponding recipient region should not also be present.

For example, if 100% of the expected funding is going to Uganda, the activity should not also	specify that the funding is going to the region of Africa:

.. code-block:: xml

  <recipient-country code=”UG” percentage=”100” />

However, if the publisher knows that at least 80% of the expected funding is going to Uganda, then the activity can specify that the unknown 20% is going to the region of Africa. Please note that an activity can specify the region from multiple region codelists:

.. code-block:: xml

  <recipient-country code=”UG” percentage=”80”/>
  <recipient-region code=”298” vocabulary=”1” percentage=”20”/>
  <recipient-region code=”002” vocabulary=”2” percentage=”20”/>

The above example shows country and region information being published at activity level. This information could instead be published at transaction level, with each transaction containing either one recipient country or one recipient region. Please note that countries and regions must not be specified at both activity and transaction levels.

IATI recommends that publishers provide geographic (country and region) and :doc:`thematic (sectors) <activity-thematic-focus>`. information at the same level. This should be consistent across all activities published by an organisation i.e. publishing **either** at activity level **or** for all transactions.

It is up to each publisher to define what they class as an activity and what their scope is e.g. global, national or within a single location). The scope of the activity should be published using the `activity-scope <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/activity-scope/>`__ element.

Rules for publishing multiple countries and regions
---------------------------------------------------

1) Every activity should have **either** a recipient country **or** a recipient region.

2) This should either be published **either** at activity level **or** once for each transaction.

3) If multiple countries and/or regions are published at activity level, the countries and regions must be given a percentage.

4) The percentage of the counties plus regions (within a vocabulary) must add up to 100%.

Tips for specifying country and regions
---------------------------------------

- **For truly global activities**

  Some activities, such as research, are not based in or benefiting particular countries or regions. For activities that are truly global, `region <http://reference.iatistandard.org/codelists/Region/>`__ code ‘developing countries, unspecified’ (998) and `activity scope <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/activity-scope/>`__ code ‘global’ (1), should be used.

- **For activities containing sub- (or child) activities**

  Some activities may be overarching or ‘parent’ projects with many activities within them. In this case they should include the sum of recipient countries and regions of their sub-activities.

- **For activities containing only management costs**

  Some activities only contain management costs. In this case they should provide the country where the expense is incurred.

What country and region information can be published?
-----------------------------------------------------

Please note:

-  If a recipient country is known, this is preferable to publishing a recipient region.

-  If a region is included, it must be in addition to any countries specified.

-  There is only one `country codelist <http://reference.iatistandard.org/codelists/Country/>`__ that can be used.

-  There are a number of `region codelists <http://reference.iatistandard.org/codelists/RegionVocabulary/>`__ that can be used, including an organisation’s internal list. These can be used simultaneously. Use of the DAC region codelist is recommended and should be included alongside other region codelists.

For data published at activity level:

- Multiple recipient countries and regions can be declared. Each recipient must have a percentage.

- The percentage of all recipient countries plus regions (within a specific region vocabulary) must add up to 100%.

- Multiple region vocabularies can be used. Each region vocabulary must have the same percentage share e.g. one activity can have:

  -  Country: Uganda (UG) 80%

  - DAC Region: Africa (298) 20%

  - UN Region: Africa (002) 20%

For data published at transaction level:

- Every transaction must have a recipient country or region.

- A transaction must not have more than one recipient country or region.

Technical guidance summary
--------------------------

**For geographic information published at activity level**

If geographical data is published at activity level, it must not also be published at :doc:`transaction <financial-transactions>` level.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `activity-scope <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/activity-scope/>`__
     - Describes the scope of the activity e.g. global, national or a single location.
     - This must be included no more than once for each activity.

       A code must be selected from the `activity scope <http://reference.iatistandard.org/codelists/ActivityScope/>`__ codelist.
     -

   * - `recipient-country <http://iatistandard.org/activity-standard/iati-activities/iati-activity/recipient-country/>`__
     - Specifies in what `countries <http://reference.iatistandard.org/codelists/Country/>`__ the activity took place, or which countries benefited from the activity.
     - If multiple countries or regions are published, a percentage split must be declared for each.

       The percentage published must be a decimal number between 0 and 100 inclusive, with no percentage sign.

       Percentages for all published countries and regions (within a region vocabulary) must add up to 100.

       Recipient-region must not be used merely to describe the region of a country published in recipient-country, but only if the region is a recipient in addition to the country.

       If published here, recipient country and region must not be used at transaction level.
     - If a specific country is not known the recipient-region element should be used instead.

       If the region vocabulary is not specified, the OECD DAC `region <http://reference.iatistandard.org/codelists/RegionVocabulary/>`__ codelist is assumed.

       If region vocab 99 (reporting org) is used, it is strongly recommended that a link to the codelist is included, to help users understand the meaning of the code.

       A narrative element can be used to describe the recipient country or region.

   * - `recipient-region <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/recipient-region/>`__
     - Specifies in what `regions <http://reference.iatistandard.org/codelists/RegionVocabulary/>`__ the activity took place, or which regions benefited from the activity.
     -
     -


**For geographic information published at transaction level**

If geographical data is published at transaction level it must be included for every transaction. If included here, it must not be published also at activity level.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `recipient-country <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/recipient-country/>`__
     - The specific `country <http://reference.iatistandard.org/codelists/Country/>`__ that will benefit from the transaction.
     - The country must be present on the `country <http://iatistandard.org/codelists/Country/>`__ codelist.

       Only one recipient-country or one recipient-region must be published.
     - If the specific country is not known, the recipient-region element should be used instead.

   * - `recipient-region <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/recipient-region/>`__
     - The specific `region <http://reference.iatistandard.org/codelists/RegionVocabulary/>`__ that will benefit from the transaction.
     - The region code must be on the specified `region vocabulary <http://reference.iatistandard.org/203/codelists/RegionVocabulary/>`__ used.

       Only one recipient-country or one recipient-region must be published.
     - If no vocabulary is specified the OECD DAC `region <http://reference.iatistandard.org/codelists/RegionVocabulary/>`__ codelist is assumed.

Sub-national locations
----------------------
Activities can also contain sub-national locations, these detail where an activity is happening within a country. For further details see:
- :doc:`Activity geography <activity-geography>`
- :doc:`Sub-national-locations <sub-national-locations>`

.. meta::
  :title: Geography - countries and regions
  :description: Each activity in IATI should specify the country (e.g. China) in which the activity is taking place, or the places that will benefit from the activity.
  :guidance_type: activity
