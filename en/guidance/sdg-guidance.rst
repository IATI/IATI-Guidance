How to use the IATI Standard for publishing and using data on the Sustainable Development Goals (SDGs)
=======================================================================================================

**Guidance for publishing and using SDG data in the IATI Standard**

Table of Contents
------------------

**1. How to publish SDG data**
  1.1 Publishing SDGs at activity level using <tag>
  1.2 Publishing SDGs at result level using <reference>

**2. Using SDG data in IATI**
  2.1 Different areas where SDG data can be found
  2.2 Combining Goals, Targets and Indicators
  2.3 Data use tips


**1. How to publish SDG data**
-------------------------------

IATI recommends that, if possible, you should attribute SDGs to your activities as well as to their specific results:

-  SDG Goals and Targets should be attributed to activities using the `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ element;

-  The more granular SDG Indicators should be attributed to results via the result indicator `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__ element.

If you are unsure which SDG Goals or Targets your activity relates to, it may be helpful to look at other activity classifications including sectors, policy markers and expected results you are using. Look for keywords that relate to specific SDGs.

If the activity has an SDG Indicator in its results framework, or the result relates to an SDG Indicator, the corresponding SDG Indicator code should be added to the indicator `<reference> <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__ element in the results section. The corresponding SDG Target should also be included in the `<tag> <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ element.

----

1.1 Publishing SDGs at activity level using ``tag``
----------------------------------------------------

Version 2.03 of the IATI Standard introduced the element `<tag> <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__. This allows you to ‘tag’ the whole of an activity to one or multiple SDG Goals or Targets. This will indicate which SDG Goals or Targets a given activity contributes to, without associating specific percentages, finances or priorities.

It is possible to identify SDGs at two levels, either using the 17 SDG Goals or the 169 SDG Targets. You specify what level you are using by declaring the `tag vocabulary <http://reference.iatistandard.org/codelists/TagVocabulary/>`__.

**Using the SDG Target vocabulary is recommended.**

-  **SDG Goal**: **<tag** vocabulary="2" code="8"\ **/>**

-  **SDG Target**: **<tag** vocabulary="3" code="8.8"\ **/>**

As one SDG Goal contains a number of Targets but Targets only link to one Goal, it will always be possible for data users to derive SDG Goals from reported SDG Targets (but not the other way around). Please note if you are reporting at target level, you **should not** also report the corresponding SDG Goal.

It is possible to link an activity to one or more SDG Goals or Targets. IATI does not place a limit on the number of SDG Goals or Targets you can publish in the `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ element.

**Caution:** when publishing both `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__
and `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__ elements in a single activity, you should take great care to keep the data coherent. For example, if you publish SDG Indicator 6.4.1 (which belongs to target 6.4) in the results section, ensure you also publish SDG Target 6.4 as a `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__.

*It is also likely that some SDG Targets or Goals published in* `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ *elements will not have a corresponding SDG Indicator in the results section e.g. you may publish SDG Target 1.1 in a* `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ *element without having SDG Indicator 1.1.x in the results section.*

**Example:**

In the examples below an activity is tagged to SDG Target 8.8 which relates to SDG Goal 8 (Decent Work and Economic Growth).

Note that only the code is reported in the first example. The second example shows how descriptions can be added in multiple languages. You can download translations of the SDG Goals and Targets `here <https://unstats.un.org/sdgs/indicators/indicators-list/>`__.

*Example 1:*

Tag element with no narrative:

.. code-block:: xml

  <tag vocabulary="3" code="8.8" />

*Example 2:*

Tag element with narratives in English and French:

.. code-block:: xml

  <tag vocabulary="3" code="8.8">
    <narrative xml:lang="en">Protect labour rights</narrative>
    <narrative xml:lang="fr">Défendre les droits des travailleurs</narrative>
  </tag>

1.2 Publishing SDGs at result level using ``reference``
--------------------------------------------------------

Version 2.02 of the IATI Standard introduced the `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__ element within the result indicator element. A result can be measured through multiple indicators; publishers may link each of their indicators to one SDG Indicator.

If you publish an SDG Indicator in the indicator `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__ element IATI strongly recommends that you publish the corresponding SDG Target in the `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ element. For example, if you publish SDG Indicator 6.4.1 (which belongs to target 6.4) in the results section, ensure you also publish SDG Target 6.4 as a `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__.

**SDG Indicators**

The SDG list of indicators currently contains over 200 indicators measuring progress towards the SDG Goals. Organisations can specify which SDG Indicator their own result indicator best relates or contributes to. This is done by using code 9 from the `indicator vocabulary codelist <http://reference.iatistandard.org/codelists/IndicatorVocabulary/>`__.

If an organisation’s internal indicator directly corresponds to one of the SDG Indicators, then the SDG Indicator code and name should be given as the indicator `title <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/title/>`__. The SDG Indicator code should also be specified in the `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__ element using code 9 from the `indicator vocabulary codelist <http://reference.iatistandard.org/codelists/IndicatorVocabulary/>`__.

When providing an SDG Indicator code, you should use the format 1.1.1 and not the UNSD Indicator Codes format CO10101.

Alongside this you can provide links to your own indicator codelist within the result indicator element using code 99 from the `indicator vocabulary codelist <http://reference.iatistandard.org/codelists/IndicatorVocabulary/>`__.

Please note that you can only attach **one SDG Indicator** to each of your result indicators published to IATI.

**Examples:**

Example 1:

In the example below an organisation’s reported indicator is linked to SDG Indicator 8.8.2, which is part of SDG Goal 8 (Decent Work and Economic Growth). It is also linked to the organisation’s own indicator codelist using vocabulary 99. Please note that narratives cannot be added to the reference element.

.. code-block:: xml

  <result>

**...**

.. code-block:: xml

  <indicator measure="1" ascending="1">
    <title>
      <narrative>Description of the indicator</narrative>
    </title>
    <reference vocabulary="9" code="8.8.2" />
    <reference vocabulary="99" code="1" indicator-uri="http://example.com/indicators.html" />

**...**

.. code-block:: xml

    </indicator>
  </result>

Example 2:

The example below provides a full example with more detail about linking an activity’s reported indicator with a related (not exact) SDG Indicator, in this case 6.4.1 (change in water-use efficiency over time).

*Organisation A implements a programme to improve the standards of operation of water operators in Africa, which contributes to SDG Goal 6 - “Ensure availability and sustainable management of water and sanitation for all.”*

*In order to measure its results, Organisation A has defined an indicator “Number of Water and Sanitation Service Providers that have reduced Non Revenue Water (spilled water) at utility level according to target” which relates to SDG Indicator 6.4.1 – “Change in water-use efficiency over time.”*

In IATI this looks as follows:

.. code-block:: xml

  <result type="2" aggregation-status="0">
    <title>
      <narrative>Non-Revenue Water reduction</narrative>
    </title>
    <indicator measure="2" ascending="1" aggregation-status="1">
      <title>
        <narrative>Number of Water and Sanitation Service Providers that have reduced Non-Revenue Water (spilled water) at utility level according to target.</narrative>
      </title>
      <reference vocabulary="9" code="6.4.1" />
      <baseline year="2018" value="0" />
      <period>
        <period-start iso-date="2018-01-01" />
        <period-end iso-date="2022-12-31" />
        <target value="8">
          <comment>
            <narrative>The goal is to decrease NRW levels with at least 8 partners out of 10 involved in this program.</narrative>
          </comment>
        </target>
      </period>
      <period>
        <period-start iso-date="2018-01-01" />
        <period-end iso-date="2018-12-31" />
        <actual value="1" />
      </period>
    </indicator>
  </result>

----

**2. Using SDG data in IATI**
------------------------------

2.1 Different areas where SDG data can be found
------------------------------------------------

The IATI Standard is designed to allow organisations to publish SDG data in a way that makes sense to them. IATI recommends that publishers should attribute SDGs to their activities, as well as to the results of each activity. This means when using IATI SDG data, you may be required to combine SDG data published in different parts of the IATI Standard.

IATI recommends that organisations publish SDG data in two places:

-  Goals and Targets can be published at activity level via the `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ element

-  Indicators can be published at result level via the indicator `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__ element

Both approaches involve ‘tagging’ an activity or result with either an SDG Goal, Target or Indicator. The guidance below explains how the data can be combined and used.

Please note that `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ was introduced at version 2.03. The indicator `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__ element was introduced at version 2.02.

**Exceptions (not recommended)**

It is possible that organisations will have published SDG data under the `sector <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/sector/>`__ and `policy-marker <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/policy-marker/>`__ elements. Neither of these options are recommended.

If you require help in using SDG data published in these elements, please contact: `support@iatistandard.org <mailto:support@iatistandard.org>`__. Please do also get in contact with the organisation and ask them to consider changing their publishing.

If you are building a data use tool, IATI advises that you should only include SDG data published in the `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ and indicator `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__ elements.

----

2.2 Combining Goals, Targets and Indicators
--------------------------------------------

There are three levels to the Sustainable Development Goals:

**X) Goals**

There are 17 Goals, these are broad aspirations.

*E.g. 1: End poverty in all its forms everywhere.*

**X.X) Targets**

Each Goal is broken down into multiple aspects called Targets. There is a total of 169 Targets.

*E.g. 1.1 By 2030, eradicate extreme poverty for all people everywhere, currently measured as people living on less than $1.25 a day.*

**X.X.X) Indicators**

Indicators are used to monitor the progress towards the SDG Targets and corresponding Goals. There are over 200 hundred Indicators.

*E.g. 1.1.1 Proportion of population below the international poverty line, by sex, age, employment status and geographical location (urban/rural).*

The SDGs have a numbering system which allows you to work out which Target and Goal an Indicator belongs to. For example:

&nbsp;&nbsp;&nbsp;&nbsp;Indicator 1.1.1
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Belongs to Target 1.1
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Which belongs to Goal 1.

Organisations can tag their IATI activities and results with a mixture of Goals, Targets and Indicators. This can make it harder to aggregate IATI SDG data.

However, you can transform Indicators into Targets and Targets into Goals. If an activity is tagged with Indicator 1.1.1, you know that the activity is targeting Goal 1: Ending poverty in all its forms. Using this method will allow you to aggregate and analyse SDG data from multiple publishers.

----

2.3 Data use tips
------------------

IATI recommends that SDG Indicator codes are presented in the format 1.1.1. This allows each code to be attributed to a specific SDG Target. A handful of SDG Indicators are repeated across different SDG Targets. A list of duplicated SDG Indicators can be found `here <https://unstats.un.org/sdgs/indicators/indicators-list/>`__.

A conversion to SDG Indicators in the format CO10101 can be found by downloading the excel files `here <https://unstats.un.org/sdgs/indicators/indicators-list/>`__.

IATI recommends that if a publisher’s internal indicators do not directly match any SDG Indicator, they should choose one SDG Indicator that their internal result’s indicator best relates or contributes to. Note that a publisher’s result’s indicator may contribute to multiple SDG Indicators. If you are looking to see which IATI activities contribute to a specific SDG Indicator, you are advised to first check the `tag <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/tag/>`__ element to see which activities have specified the particular SDG Goal or Target as well conducting a free word search of the activity’s narrative elements.

----
