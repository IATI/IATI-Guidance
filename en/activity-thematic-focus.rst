Activity thematic focus (sectors)
=================================

Each activity published to IATI must provide details of the thematic focus of the activity. The themes must be explained in code, and then further details can be provided in a written description. For example, an activity could be to do with ‘health’ and the description is that the activity is a vaccination programme. Or an activity could be to do with ‘education’ and the description is that the activity is training community leaders to tackle gender inequality in their communities.

The purpose of an activity must be provided by declaring a code in the <sector> element at either `activity <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/sector/>`__ or `transaction <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/sector/>`__ level. A mix of codes from different `sector vocabularies <http://reference.iatistandard.org/203/codelists/SectorVocabulary/>`__ can be used. For example, an activity can contain its publisher’s internal sector classifications alongside the `OECD DAC 5-digit <http://reference.iatistandard.org/codelists/Sector/>`__ sector codes.

IATI recommends choosing a code from the OECD DAC 5-digit sector codelist. Where possible, the activity should use specific codes rather than codes that cover general areas (for more details see `here <http://reference.iatistandard.org/activity-standard/overview/country-budget-alignment/>`__).  For example, an activity can include multiple codes such as ‘basic health care’ (12220) and ‘women’s equality organisations and institutions’ (15170), instead of the very general ‘multisector aid’ (43010).

The OECD DAC 5-digit codes cover a wide range of humanitarian and development work. This then allows data users to compare and analyse all the data in IATI, as data can be searched and filtered by these sector codes.

    More thematic data can be added to activities by attaching references to the Sustainable Development Goals (SDGs). For additional guidance on how to publish data for the SDGs, see :doc:`here <sdg-guidance>`.

Using multiple sector codes
---------------------------

Where more than one sector code is used from a vocabulary, a percentage for each different sector code must be included. If the activity has only one sector, it is presumed that 100% of the funding is going to that sector. A sector can also be specified from multiple vocabularies.

When multiple sectors from the same vocabulary are published, the percentage for each must add up to 100%.

For example, if 100% of the expected funding is going on teacher training, it can be published using the 5-digit DAC codelist. This can also be published against a publisher’s internal classification e.g. Primary schools work’ (A1):

.. code-block:: xml

    <sector vocabulary="1" code="11130" percentage="100" />
    <sector vocabulary="99" vocabulary-uri="http://example.com/vocab.html" code="A1" percentage="100" >
      <narrative>Internal classification - primary schools work</narrative>
    </sector>

However, if the activity can be split between two DAC sector codes, this can be published as 50% of the funding going to the DAC sector code ‘teacher training’ (11130) and 50% to ‘primary education’ (11220). In this example both DAC sector codes fit into the publisher's internal classification, primary schools work’ (A1):

.. code-block:: xml

    <sector vocabulary="1" code="11130" percentage="50" />
    <sector vocabulary="1" code="11220" percentage="50" />
    <sector vocabulary="99" vocabulary-uri="http://example.com/vocab.html" code="A1" percentage="100" >
      <narrative>Internal classification - primary schools work</narrative>
    </sector>

The above example shows thematic (sector) information being published at an activity level. This information could instead be published at transaction level, with each transaction containing one sector code. However, this should be consistent across **all** activities published by an organisation i.e. publishing all sector information at **either** activity level **or** for all transactions.

IATI also recommends publishers provide thematic (sectors) information and :doc:`geographic (countries and regions) <countries-regions>` information at the same level. This should be consistent across **all** activities published by an organisation i.e. publishing either at activity level or for all transactions.

**Rules for publishing sectors:**

1) Every activity must have at least one sector code.

2) Sector codes must be published at **either** activity level **or** once for each transaction.

3) If multiple sectors from the same vocabulary are published at activity level, the sectors must be given a percentage.

4) The percentage of the sectors within a vocabulary must add up to 100%.

What sector information can be published?
-----------------------------------------

Please note:

Sector codes must only be used at either activity or transaction level.

**At activity level**:

- Multiple sectors can be specified from the same `vocabulary <http://reference.iatistandard.org/codelists/SectorVocabulary/>`__.

- When multiple sectors from the same vocabulary are described, a percentage must be declared for each. All published sectors from the same vocabulary must add up to 100%.

- If no `vocabulary <http://reference.iatistandard.org/codelists/SectorVocabulary/>`__ is declared, then the `OECD DAC 5-digit <http://reference.iatistandard.org/codelists/Sector/>`__ codelist is assumed.

- A publisher can declare their own `vocabulary <http://reference.iatistandard.org/codelists/SectorVocabulary/>`__ by using the 98 or 99 (Reporting Org) vocabulary code.

- When using vocabulary codes 98 or 99, a narrative must be added to describe the sector code being used. The narrative should **not** be included for any other vocabulary codes.

**At transaction level:**

- Every :doc:`transaction <financial-transactions>` must have a sector code.

- Only one sector code from each vocabulary must be used.

-  If no `vocabulary <http://reference.iatistandard.org/codelists/SectorVocabulary/>`__ is declared, then the `OECD DAC 5-digit <http://reference.iatistandard.org/codelists/Sector/>`__ codelist is assumed.

- A publisher can declare their own vocabulary by using the 98 or 99 (Reporting Org) vocabulary code.

- When using vocabulary codes 98 or 99, a narrative must be added to describe the sector code being used.

- It is recommended that the same narrative is used for the same self-defined sector codes within a dataset.

Technical guidance summary: activity level
------------------------------------------

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `sector <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/sector/>`__
     - Specifies the purpose of the activity.

       Sector codes can come from `multiple vocabularies <http://reference.iatistandard.org/codelists/SectorVocabulary/>`__, including an organisation’s internal list.
     - Sector must either be published here or for every transaction.

       If multiple sectors are published, then each vocabulary’s percentage must add up to 100%.

       If `sector vocabulary <http://reference.iatistandard.org/codelists/SectorVocabulary/>`__ 98 or 99 is used, the narrative element must be included.
     - It is recommended that `OECD DAC 5-digit <http://reference.iatistandard.org/codelists/Sector/>`__ codes are used. Other codes can be added in addition to this.

       If no codelist is declared, the OECD DAC 5-digit codelist is presumed.

       If vocabulary 98 or 99 (reporting org) is used, it is strongly recommended that a link to the codelist is included. This helps ensure that users can understand the meaning of the code.

   * - `narrative <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/sector/narrative/>`__
     - A description of the sector.
     -
     - The narrative should only be used when vocabularies 98 or 99 are used. It is recommended that the narrative used for the same self-defined sector codes is consistent within a dataset.

       The narrative can be repeated in multiple languages.

       If the language differs from the default language, the language should be declared using the language attribute.


Technical guidance summary: transaction level
---------------------------------------------
If thematic (sector) data is published at transaction level it must be included for every :doc:`transaction <financial-transactions>`. If included here it must not be published at activity level.

.. list-table::
   :widths: 26 28 28 28
   :header-rows: 1

   * - Element
     - Use
     - Rules
     - Guidance

   * - `sector <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/sector/>`__
     - Specifies the purpose of the activity.

       Sector codes can come from `multiple vocabularies <http://reference.iatistandard.org/codelists/SectorVocabulary/>`__, including an organisation’s internal list.
     - Sector must either be published here or must be published at the activity level.

       Multiple sectors can be published, but there must only be one code from each `sector vocabulary <http://reference.iatistandard.org/codelists/SectorVocabulary/>`__.
     - It is recommended that an `OECD DAC 5-digit <http://reference.iatistandard.org/codelists/Sector/>`__ code is used. Other codes can be added in addition to this.

       If no codelist is declared, the OECD DAC 5-digit codelist is presumed.

       If the `sector vocabulary <http://reference.iatistandard.org/codelists/SectorVocabulary/>`__ 98 or 99 is used, the narrative element should be included.

   * - `narrative <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/sector/narrative/>`__
     - A description of the sector.
     -
     - The narrative should only be used when vocabularies 98 or 99 are used.

       The narrative can be repeated in multiple languages.

       If the language differs from the default language, the language should be declared using the language attribute.


.. meta::
  :title: Activity thematic focus (sectors)
  :description: Each activity published to IATI must provide details of the thematic focus of the activity. The themes must be explained in code, and then further details can be provided in a written description.
  :guidance_type: activity
  :date: September 19, 2019
