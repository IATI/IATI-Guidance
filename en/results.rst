Results information
===================

Results describe the benefit or intended benefits of an activity; these can be broken down into `types <http://reference.iatistandard.org/codelists/ResultType/>`__: outputs, outcomes and impacts. Updating results regularly means that data users can track an activity’s progress and learn from other organisation’s activities - such as whether or not the activity was a success and what challenges were faced. Both positive and negative results should be included.

IATI offers a rich structure, allowing organisations to publish results which are meaningful to them. Publishers are able to link their results to agreements with their donors e.g., by coordinating results publishing with their partners, alliance and/or stakeholders. Often, the published results will relate to the framework of the agreed objectives for the activity, or activities. There is no single way to publish results in IATI and this can make results hard to understand. This guidance helps explain what can be captured in the IATI Standard.

How results data is published will depend on the structure of an organisation’s activities and their results frameworks. For example, if a programme is being published, overarching results details may be published in the parent activity, with more detailed results being published in the sub (child) activities. Or, if the publisher is working in an alliance, each organisation could publish results using the same indicators so that their results are comparable.

To better understand publishing and using results data, it may be helpful to look at a visualisation. `d-portal <http://www.d-portal.org/>`__ is one tool that helps to visualise results data, for further information see :doc:`Understanding results data <understanding-results>`.

*Please note, security implications may also prevent results data from being published, or require results to be aggregated. Any security considerations should be outlined in an organisation’s* `exclusion policy <https://iatistandard.org/en/guidance/preparing-organisation/organisation-data-publication/information-and-data-you-cant-publish-exclusions/>`__\ *.*


Understanding Results
---------------------

There are many elements and attributes that can be used and not all may be needed. For organisations wanting to publish results data, IATI recommends first thinking about **what** the results are that they want shown and then looking at **how** they can be mapped onto the IATI Standard.

Results in IATI are generally one of three types:

-  **Output (1)**: A direct consequence of the activity, e.g. vaccinations delivered to X number of children.

-  **Outcome (2)**: A short term effect the activity has contributed to, e.g. lower rates of infection after a vaccination programme.

-  **Impact (3)**: A long term effect the activity has contributed to, e.g. improved life expectancy.

Each activity can have multiple results of each type, i.e. multiple outputs.


**Measuring results**

Each result is measured by one or more indicators. For example, the number of different types of vaccines provided and how many local staff were trained to give them.

Each indicator can have a given time period with a start and an end date. This is the time period in which the indicator is being measured, e.g. agricultural season or school term. A baseline value shows the progress at the beginning of the time period. Often, the baseline is 0 as no work has yet been carried out. A target value provides the progress that should have been achieved by the end of the period. The actual value provides the progress that was achieved during the given time period. You can track the progress of an indicator over time; to enable this an indicator needs to have multiple time periods. e.g. yearly time periods for 2018, 2019 and 2020.

The indicator description can be used to help explain what’s being measured and how. For example, whether the published values are aggregatable (the data user should add them up to get the total) or cumulative (the data user should look at the most recent value to get the total).

*Please note, the indicators for different types of results (outputs, outcomes and impacts) will often be measured across different time periods, ranging from a few days to multiple years.*

Each indicator must have a measure attribute; this describes what the indicator is being measured in. The three most common `measure types <http://reference.iatistandard.org/codelists/IndicatorMeasure/>`__ in IATI are:

**Numerical (quantitative) measures**

-  **Unit (1)**: e.g. number of workshops delivered.

-  **Percentage (2)**: e.g. percentage of the population who have received a vaccine.

Indicators with these measures should have numerical `baseline <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/>`__, `target <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/target/>`__ and `actual <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/>`__ indicator values. If a high number shows improvement, the ‘ascending’ boolean should be set to 1 (true). If a low number shows improvement, the ‘ascending’ boolean should be set to 0 (false).

**Descriptive measures**

-  **Qualitative (5)**: e.g. this is often a description, such as detailing more favourable attitudes towards gender equality amongst trained staff

Indicators with this measure type should have descriptive `baselines <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/comment/>`__, `targets <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/target/comment/>`__ and `actuals <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/comment/>`__. This is captured within the comment elements; the value attribute should not be published.

Indicators can also be linked to existing results frameworks, e.g. the Sustainable Development Goal Indicators. For more information on how to do this please see: :doc:`How to use the IATI Standard for publishing and using data on the Sustainable Development Goals (SDGs) <sdg-guidance>`.

Different donors have their own requirements when it comes to publishing results. Guidance from each donor can be found on the `Donors Reporting Requirements <https://iatistandard.org/en/guidance/preparing-data/donors-reporting-requirements/>`__ page.

**Example usage**

An activity is working towards the outcome that ‘people to have access to independent media covering a diverse range of outcomes’ (title). One of the ways this is being measured is through ‘the percentage of journalists who feel free to express their opinion’ (indicator). This is measured through a bi-annual survey where they are asked to score how free they feel on a scale of 1 - 4.

The starting value (baseline) was 15% of journalists felt free to express their opinions. At the end of the chosen time period, the target was set at 50%. The activity did meet its target, as by the end of the period (actual) 53% of journalists felt free to express their opinions.

.. code-block:: xml

    <result type="2">
      <title>
        <narrative>People who have access to independent media covering diverse options.</narrative>
      </title>
      <description>
        <narrative>Further explanation of the expected result.</narrative>
      </description>
      <indicator measure="2" ascending="1" >
        <title>
          <narrative>The percentage of journalists who feel free to express their opinion (scoring 3 or 4)</narrative>
        </title>
        <description>
          <narrative>
            1 = Not at all free
            2 = No, not entirely free
            3 = Yes, up to some level
            4 = Yes, entirely free
            This is measured through a bi-annual survey amongst journalists.
          </narrative>
        </description>
        <baseline year="2012" value="15">
	        <comment>
            <narrative>Baseline measured in a survey amongst 1083 journalists in country x.</narrative>
          </comment>
        </baseline>
        <period>
          <period-start iso-date="2012-01-01" />
          <period-end iso-date="2015-12-31" />
          <target value="50" />
          <actual value="53" />
        </period>
      </indicator>
      <indicator>

        ...

.. code-block:: xml

      </indicator>
    </result>


Results should include
----------------------

-  A publisher should only publish results about their own work. If working in an alliance or partnership, coordinating results publishing is highly encouraged.

-  Each activity can contain multiple results, each of which can contain multiple indicators.

-  Different types of results can be published e.g. outputs, outcomes and impacts

-  Result indicators can be measured differently e.g. using units, percentages or qualitative measures.

-  Every result must include an `indicator <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/>`__, which in turn can detail a `period <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/>`__ of time, and then a `baseline <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/comment/>`__, `target <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/target/>`__ and `actual <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/>`__ measure.

-  If possible, the period in which an indicator is measured should be meaningful to the activity e.g. agricultural seasons or school terms.

-  Numerical (quantitative) baseline, target and actual measures should be published in the value attributes.

-  The ascending boolean details whether high numerical values are good (1 = true) or if low numerical values are good (0 = false)

-  Descriptive (qualitative) baselines, targets and actual measures should be published in the comment elements.

-  Comment elements can also be used to help describe results and indicators. These can be published in multiple languages.

-  Each indicator can have a `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__, linking it to an external framework (for example, the :doc:`SDG Indicators <sdg-guidance>`). It is recommended that publishers include this for each indicator, and not for each result.


Technical guidance summary
--------------------------

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `result <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/>`__
     - This contains information about the result of the activity.
     - The `type <http://reference.iatistandard.org/codelists/ResultType/>`__ of result must be published e.g. output, outcome or impact.
     - Multiple results can be published.

       The result can flag whether or not the data is suitable for aggregation using the @aggregation-status flag.

   * - `title <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/title/>`__
     - This is the title of the result.
     - This element must appear only once within each result element.
     - The title can be repeated in multiple languages using the `narrative <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/title/narrative/>`__ element.

   * - `description <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/description/>`__
     - The description provides more detail about the result.
     - This element must appear only once within each result element.
     - The description can be repeated in multiple languages using the `narrative <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/description/narrative/>`__ element.

   * - `document-link <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/document-link/>`__
     - A link to an online, publicly accessible web page or document expanding on the result.
     -
     - Further guidance can be found on the :doc:`Related documents <related-documents>` page.


**Publishing Indicators**

Multiple indicators can be published for each result. These describe how the activity’s progress towards the result is measured.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `indicator <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/>`__
     - This contains information about the indicator of the result.
     - This element must appear at least once within each result element.

       How the indicator is being `measured <http://reference.iatistandard.org/codelists/IndicatorMeasure/>`__ must be included e.g. in units, percentages or qualitative narrative.

     - The element can specify whether or not the indicator is ascending or descending and if the data is suitable for aggregation.

   * - `title <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/title/>`__
      - This is the title of the indicator.
      - This element must appear only once within each indicator element.
      - The title can be repeated in multiple languages using the `narrative <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/title/narrative/>`__ element.

    * - `description <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/description/>`__
      - The description provides more detail about the indicator.
      - This element must appear only once within each indicator element.
      - The description can be repeated in multiple languages using the `narrative <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/description/narrative/>`__ element.

    * - `document-link <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/document-link/>`__
      - A link to an online, publicly accessible web page or document expanding on the indicator.
      -
      - Further guidance can be found on the :doc:`Related documents <related-documents>` page.

    * - `reference <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/reference/>`__
      - A standardised means of identifying the indicator from a code in a recognised vocabulary.
      - Multiple vocabularies may be specified, but each vocabulary must be specified only once for each indicator.

        Reference can be published here or at results level but not both.

      - If `indicator vocab <http://reference.iatistandard.org/codelists/IndicatorVocabulary/>`__ 99 (reporting org) is used, it is strongly recommended that a link to the codelist is included. This helps ensure that users can understand the meaning of the code.

        This element can be used to link SDG Indicators to the published indicator. Further guidance is :doc:`here <sdg-guidance>`.


**Publishing baselines, targets and actuals**

The values of each indicator are published in the following `baseline <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/>`__, period `target <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/target/>`__ and period `actual <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/>`__ elements. The baseline is the starting point. The target is a result an organisation wants an activity to achieve in a certain period of time. The actual is what was achieved at the end of that period.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `baseline <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/>`__
     - Holds the baseline value for the indicator.
     - The year (yyyy) the value was taken must be included.

       A value must be included for all non-qualitative measures.

     - A specific date of when the value was taken can be published.

       The value attribute should be omitted for qualitative measures. The value attribute should be a valid number for all non-qualitative measures.

       If publishing a qualitative measure, the narrative should be provided in the `comment <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/comment/>`__ element.

   * - `dimension <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/dimension/>`__
     - A category used for disaggregating the results by gender or age, etc.

       A name and value for the aggregation can be provided.

     -
     - For example an activity could declare the dimension’s name as *sex*, with a value of *female*.

     - A baseline can have multiple dimensions.

   * - `document-link <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link/>`__
     - A link to an online, publicly accessible web page or document expanding on the baseline.
     -
     - Further guidance can be found on the :doc:`Related documents <related-documents>` page.

   * - `comment <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/comment/>`__
     - Further describes the baseline and describes qualitative results.
     - This element must appear only once within each baseline element.
     - The comment can be repeated in multiple languages using the `narrative <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/comment/narrative/>`__ element.


**Publishing target and actual values in a given time period**

The period element defines the period of time in which the organisation is measuring the indicator. Multiple periods and measures can be published.

The period element includes target and actual values. Target and actual contain the same elements and attributes as the baseline element. See the table above on how to publish on these.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `period <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/>`__
     - Defines the period in which the indicator is being measured.
     -
     - Multiple periods can be published.

   * - `period-start <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/period-start/>`__
     - The start of the period.
     - This must be published and only occur once within each period element.

       The date must be in the format (YYYY-MM-DD).

       The start date must be before, or the same as, the end date.

     -

   * - `period-end <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/period-end/>`__
     - The end of the period.
     - This must be published and only occur once within each period element.

       The date must be in the format (YYYY-MM-DD).

       The end date must be after, or the same as, the start date.

     -

   * - `target <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/target/>`__
     - Defines the target value for this period.
     -
     - Multiple targets can be published for each period.

      Target contains the same elements and attributes as baseline. See the table above for further guidance.

   * - `actual <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/>`__
     - Defines the actual value achieved at the end of this time period.
     -
     - Multiple actuals can be published for each period.

       Actual contains the same elements and attributes as baseline. See the table above for further guidance.


.. meta::
  :title: Results information
  :description: Results describe the benefit or intended benefits of an activity; these can be broken down into types: outputs, outcomes and impacts.
  :guidance_type: activity
  :date: July 27, 2020
