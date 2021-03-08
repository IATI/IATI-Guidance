How to publish humanitarian data
================================

Version 2.03 of the IATI Standard contains a number of new and enhanced elements and attributes. These, along with the humanitarian flag attribute introduced at v2.02, allow publishers to mark their activities as humanitarian. This guidance has been developed with the humanitarian community and is intended to help with the alignment and import of humanitarian IATI data into UN OCHA’s Financial Tracking Service (FTS), as well as meeting Grand Bargain transparency commitments.

It is up to each publisher to determine whether an activity should be categorised as humanitarian and whether the activity is partially or wholly humanitarian. These distinctions can then be included in an organisation's IATI data using the humanitarian elements and attributes described below.

In the event of any rapid onset or other emergency it is recommended that publishers update and re-publish humanitarian activities on a daily or at least a weekly basis in order that the most up-to-date information is continually available to data users.


How to use the humanitarian elements and attributes:
----------------------------------------------------

Please see the guidance below on the seven areas in which humanitarian data can be published in IATI activity files.

1) Identifying humanitarian activities - humanitarian flag
2) Using humanitarian OECD DAC 5-digit sector codes
3) Humanitarian scope - GLIDE codes and UN Humanitarian Response Plan (HRP)
4) Publishing humanitarian budgets - budget-not-provided attribute
5) Identifying local actors - participating organisation types
6) Linking to Humanitarian Global Clusters
7) Classifying contributions: earmarking, cash and / or vouchers - Aid Type

**Note: It is up to each organisation to decide on the humanitarian elements and attributes to be included in their data.**

1) Identifying humanitarian activities
--------------------------------------

The primary way of identifying humanitarian activities is by including the humanitarian flag at activity level.

.. list-table::
   :widths: 50 50
   :header-rows: 1


   * - Name
     - Type

   * - Humanitarian Flag (IATI Standard version 2.02, 2.03)
     - Attribute (boolean)

**Example:**

.. code-block:: xml

  <iati-activity humanitarian="1">

This is a yes/no flag which indicates that an activity relates entirely or partially to humanitarian aid. Each flag must have either the value **1 = humanitarian** or **0 = development**.

Activities with the humanitarian flag set to 1, can be either wholly or partially humanitarian.

**Identifying humanitarian transactions**

The humanitarian flag can also be added to transactions.

The humanitarian flag at transaction level should only be used if the transactions can be separated into humanitarian and development components. In this case, each transaction should be given a humanitarian flag of value **1 = humanitarian** or **0 = development**.

**Example:**

.. code-block:: xml

 <transaction ref="1234" humanitarian="0">
 <transaction ref="2345" humanitarian="1">

2) Using humanitarian OECD DAC 5-digit sector codes
---------------------------------------------------

.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Name
     - Type

   * - Sector
     - Element

**Example:**

.. code-block:: xml

  <sector vocabulary="1" code="72010" />

Every activity reported to IATI must include at least one sector element. IATI recommends that sector vocabulary 1, the OECD DAC 5-digit sector codelist is used. These sector codes cover a wide range of humanitarian and development work. For further guidance on sectors see: :doc:`Activity Thematic Focus (Sectors) </activity-thematic-focus>`.

Specific humanitarian `5 digit DAC sector codes <https://iatistandard.org/codelists/sector>`__ currently range from 72010 to 74020 and 93010 to 93018. The humanitarian code or codes that best describe the activity, or humanitarian component(s) of an activity taking place can be added to any IATI activity marked with the ‘humanitarian’ flag.

Multiple sector codes can be used. If an activity has both a humanitarian and development component at least two sector codes are needed. For example, this could be reported as 60% of the funding going to the OECD DAC sector code ‘emergency food and assistance’ (72040) and 40% going to ‘basic nutrition’ (12240):

**Example:**

.. code-block:: xml

  <sector vocabulary="1" code="72040" percentage="60" />
  <sector vocabulary="1" code="12240" percentage="40" />

3) Humanitarian scope
---------------------

.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Name
     - Type

   * - Humanitarian-scope 
     - Element

**Example:**

.. code-block:: xml

  <humanitarian-scope type="1" vocabulary="1-2" code="EQ-2015-000048-NPL">
    <narrative>Nepal Earthquake April 2015<narrative>
  </humanitarian-scope>

.. code-block:: xml

  <humanitarian-scope type="2" vocabulary="2-1" code="FNPL15">
    <narrative>Nepal Earthquake Flash Appeal 2015</narrative>
  </humanitarian-scope>

The ‘humanitarian-scope’ element can be used to identify the specific emergency and/or appeal that an IATI activity is in response to. Where possible, publishers should use a recognised code to identify both the emergency and appeal.

* Emergencies (type 1) should have a corresponding GLIDE number (vocabulary 1-2)
* Appeals (type 2) should have a corresponding Plan Code provided by UN OCHA (vocabulary 2-1). An additional vocabulary (99) can be used where publishers wish to identify a plan specified by other humanitarian agencies.

**Linking to an emergency (vocabulary 1-2)**

Emergencies can be uniquely identified by their ‘GLIDE number’.

Each emergency registered on `GLIDE <https://glidenumber.net/glide/public/search/search.jsp>`__ has its own unique code which is year and country specific. The format for these codes is: [Emergency Type] + [Year] + [Number] + [Country].

If an activity covers a complex emergency that is multi year and/or multi country, multiple GLIDE references should be included. These should be added by reporting multiple humanitarian-scope elements.

**Linking to an appeal (vocabulary 2-1)**

Appeals can be identified by their ‘Plan code’ and often consist of flash appeals and humanitarian response plans (HRPs). These codes are created by UN OCHA for use in their Financial Tracking Service (FTS).

Each appeal has its own unique plan code which covers one country, or one region, for one year.

If no recognised code to identify the emergency or appeal is available, publishers can use vocabulary code ‘99’ to declare a code from another public list. A URL for the public list and a description of the emergency or appeal should be provided: For example:

.. code-block:: xml

  <humanitarian-scope type="1" vocabulary="99" code="5" vocabulary-uri="http://www.example.com/appeals.html">
   	<narrative>Mali Refugee Crisis 2013</narrative>
  </humanitarian-scope>

For relevant guidance on use of the humanitarian-scope element to identify COVID-19 related activities see :doc:`COVID-19 related data </covid-19>`.

4) Publishing humanitarian budgets
----------------------------------

.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Name
     - Type

   * - Budget-not-provided (2.03+)
     - Attribute

**Example:**

.. code-block:: xml     

  <iati-activity humanitarian="1" budget-not-provided="3">

This attribute can be used to explain why an activity does not contain any :doc:`activity budget </activity-budgets>` elements. It must only be used when no budget elements are reported.

Activities related to rapid onset emergencies often do not have an established budget. The budget-not-provided codelist provides three reasons why no budget is reported. In the case of humanitarian emergencies, `Rapid Onset Emergency <https://iatistandard.org/codelists/budgetnotprovided>`__ (code 3), should be used.

Humanitarian activities, with expected transaction spend, which are not rapid onset emergencies should have a reported budget.

5) Identifying local actors
---------------------------

.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Name
     - Type

   * - Participating-org / type
     - Attribute

**Example:**

.. code-block:: xml  

  <participating-org ref="CC-CCC-123456789" role="4" type="24">
    <narrative>Organisation Name</narrative>
  </participating-org>

The `organisation type <https://iatistandard.org/codelists/organisationtype>`__ attribute identifies the type of each organisation that is participating in an activity, for example:

* International NGO = Oxfam GB
* National NGO = Seatini (Uganda)
* Regional NGO = African Center for Economic Transformation (ACET)

With the rising importance of enabling more locally led humanitarian responses and for the purposes of tracking commitments around localising aid to partner country-based NGOs, a new organisation type (24 - Partner Country based NGO) was added in v2.03. The NGO organisation types available in IATI are listed below. Please note that some are pending descriptions.

**Organisation types available for NGOs**

.. list-table::
   :widths: 16 42 42
   :header-rows: 1

   * - Code
     - Name
     - Description

   * - 21
     - International NGO
     -

   * - 22
     - National NGO
     -

   * - 23
     - Regional NGOs
     -

   * - 24
     - Partner Country based NGO
     - Local and National NGO / CSO based in aid/assistance recipient country

The name and type of an organisation receiving funds should also be added to each transaction, using the `receiver-org element <https://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/receiver-org>`__. See the :doc:`Financial Transactions </financial-transactions>` page for further guidance.

6) Linking to Humanitarian Global Clusters
------------------------------------------

.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Name
     - Type

   * - Sector
     - Element

**Example:**

.. code-block:: xml  

  <sector vocabulary="10" code="4" percentage="50" />
  <sector vocabulary="10" code="7" percentage="50" />

The `humanitarian response clusters <https://www.humanitarianresponse.info/en/about-clusters/what-is-the-cluster-approach>`__ are established by groups of humanitarian organisations to support coordination in a crisis response. Each cluster is formed of organisations (including both UN agencies and NGOs) tackling a main area of humanitarian action, e.g. water, health or logistics. The groups are designated by the Inter-Agency Standing Committee (IASC) and have clear responsibilities for coordination in emergencies.

Humanitarian Global Clusters can be specified in IATI data using the sector element. These can be provided alongside the OECD 5-digit DAC sector codes. The page :doc:`Activity Thematic Focus (Sectors) </activity-thematic-focus>` contains specific guidance on how to use sectors in IATI.

Multiple clusters can be added as long as a percentage split is included. The percentage split details the share of expected funding going to the particular cluster. All percentages from the same vocabulary must add up to 100%.

The Humanitarian Global Clusters can be provided using vocabulary 10 (according to the `sector vocabulary codelist <https://iatistandard.org/codelists/sectorvocabulary>`__). The codes can be downloaded by following the links on the vocabulary page. IATI does not maintain a separate list of the codes.

7) Classifying contributions: earmarking, cash and / or vouchers
----------------------------------------------------------------

.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Name
     - Type

   * - Default-aid-type 
     - Element

**Example:**

.. code-block:: xml
     
  <default-aid-type vocabulary="1" code="CO1" />
  <default-aid-type vocabulary="2" code="4" />
  <default-aid-type vocabulary="4" code="1" />
  
.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Name
     - Type
          
   * - Transaction / aid-type
     - Element

**Example:**
     
.. code-block:: xml

  <aid-type vocabulary="1" code="CO1" />
  <aid-type vocabulary="2" code="4" />
  <aid-type vocabulary="4" code="1" />

The aid-type elements can be used to add classifications to activities and their transactions. In v2.03, IATI added the ability to provide specific humanitarian classifications including the level of earmarking and whether or not funding is being provided via cash and / or vouchers.

These classifications should be declared alongside the use of the OECD DAC aid type categories ( `vocabulary 1 <https://iatistandard.org/codelists/aidtypevocabulary>`__) e.g. budget support or debt relief. When using the aid type elements, the default-aid-type applies to the whole activity, but can be overridden within a single transaction. See the page :doc:`Additional Activity Classifications </activity-classifications>` for further guidance.

**Declaring earmarked contributions**

Part of the `Grand Bargain commitment <https://interagencystandingcommittee.org/about-the-grand-bargain>`__ is to reduce the earmarking of donor contributions. To measure this, two new classification systems of earmarking modalities have been included in IATI. These appear in the form of `Aid Type Vocabularies <https://iatistandard.org/codelists/aidtypevocabulary>`__ 2 and 3.

The Earmarking Category codes (vocabulary 2) are:

.. list-table::
   :widths: 16 42 42
   :header-rows: 1

   * - Code
     - Name
     - Description

   * - 1
     - Unearmarked
     - Any or all of the Earmarking Modality code A, B or C.

   * - 2
     - Softly Earmarked
     - Any or all of the Earmarking Modality code A, B or C.

   * - 3
     - Earmarked
     - Any or all of the Earmarking Modality code G or H.

   * - 4
     - Tightly Earmarked
     - Any or all of the Earmarking Modality code I, J or K.

A breakdown of each category can be found in the `Earmarking Modality <https://reliefweb.int/sites/reliefweb.int/files/resources/Grand_Bargain_final_22_May_FINAL-2.pdf>`__ codelist (vocabulary 3, see Annex 1).

**Declaring cash and voucher assistance**

The `Grand Bargain commitment <https://interagencystandingcommittee.org/about-the-grand-bargain>`__ also asked signatories to increase the use of cash and voucher assistance. Transactions can be classified as being part of a cash and / or voucher programme, using the aid-type element at the transaction level. Definitions of the codes have been aligned with the `CaLP Glossary <https://www.calpnetwork.org/library>`__.

Each transaction should only have one aid-type per vocabulary. Transactions should be disaggregated by cash transfer and voucher modalities.

The `Cash and Voucher Modalities <https://iatistandard.org/codelists/cashandvouchermodalities>`__ codes (vocabulary 4) are:

.. list-table::
   :widths: 16 42 42
   :header-rows: 1

   * - Code
     - Name
     - Description (shortened)

   * - 1
     - Cash Transfer
     - The provision of assistance in the form of money - either physical currency or e-cash - to recipients (individuals, households or communities).

   * - 2
     - Voucher
     - A paper, token or e-voucher that can be exchanged for a set quantity or value of goods or services.

Humanitarian elements and attributes to use at activity level
-------------------------------------------------------------

+----------------------------------------------------------------------------------------------------------------------------------------+----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
| Element                                                                                                                                | Attribute            | Use                                                                                                   | Rules                                                                     | Guidance                                                  |
+----------------------------------------------------------------------------------------------------------------------------------------+----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
| `iati-activities <https://iatistandard.org/activity-standard/iati-activities>`__                                                       | @version             | A `number <https://iatistandard.org/codelists/version>`__                                             | This element must appear only once for each activity.                     | Version 2.03 or higher is needed for data to contain      |
|                                                                                                                                        |                      | indicating the IATI specification version in use.                                                     |                                                                           | all humanitarian elements.                                |
+----------------------------------------------------------------------------------------------------------------------------------------+----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
| `iati-activity <https://iatistandard.org/activity-standard/iati-activities/iati-activity>`__                                           | @humanitarian        | A yes/no flag which indicates that this activity relates entirely or partially                        |                                                                           | Available values:                                         |
|                                                                                                                                        |                      | to humanitarian aid.                                                                                  |                                                                           |                                                           |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | 1 = humanitarian                                          |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | 0 = development                                           |
|                                                                                                                                        +----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
|                                                                                                                                        | @budget-not-provided | A `code <https://iatistandard.org/codelists/budgetnotprovided>`__                                     | The attribute must only be used when no budget elements are present.      | In the case of humanitarian emergencies, code 3: Rapid    |
|                                                                                                                                        |                      | indicating the reason why this activity does not contain any budget elements.                         |                                                                           | Onset Emergency, should be used.                          |
+----------------------------------------------------------------------------------------------------------------------------------------+----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
| `participating-org <https://iatistandard.org/activity-standard/iati-activities/iati-activity/participating-org>`__                     | @type                | Specifies the `type <https://iatistandard.org/codelists/organisationtype>`__                          |                                                                           | Where possible, in country organisations should be        |
|                                                                                                                                        |                      | of organisation involved in the activity.                                                             |                                                                           | identified.                                               |
+----------------------------------------------------------------------------------------------------------------------------------------+----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
| `sector <https://iatistandard.org/activity-standard/iati-activities/iati-activity/sector>`__                                           | @vocabulary          | Specifies the `vocabulary <https://iatistandard.org/codelists/sectorvocabulary>`__                    | Sector must either be reported here or for every transaction.             | It is recommended that vocabulary 1: OECD DAC 5-digit     |
|                                                                                                                                        |                      | the sector code is from.                                                                              |                                                                           | codes is used.                                            |
|                                                                                                                                        |                      |                                                                                                       | If multiple sectors are reported, then each vocabulary’s percentage       |                                                           |
|                                                                                                                                        |                      |                                                                                                       | must add up to 100%.                                                      | In humanitarian contexts, vocabulary 10: Humanitarian     |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | Global Clusters (Inter-Agency Standing Committee) should  |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | also be used.                                             |
|                                                                                                                                        +----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
|                                                                                                                                        | @code                | Specifies the code from a particular vocabulary.                                                      |                                                                           | DAC-5 digit humanitarian codes are those between 72010    |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | and 74020 inclusive.                                      |
+----------------------------------------------------------------------------------------------------------------------------------------+----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
| `humanitarian-scope <https://iatistandard.org/activity-standard/iati-activities/iati-activity/humanitarian-scope>`__                   | @type                | A `code <https://iatistandard.org/codelists/humanitarianscopetype>`__                                 |                                                                           | Available values:                                         |
|                                                                                                                                        |                      | for the type of event or action being classified.                                                     |                                                                           |                                                           |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | 1 = emergency                                             |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | 2 = appeal                                                |
|                                                                                                                                        +----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
|                                                                                                                                        | @vocabulary          | A code for a recognised vocabulary identifying the emergency or appeal.                               |                                                                           | Most emergencies and appeals use:                         |
|                                                                                                                                        |                      |                                                                                                       |                                                                           |                                                           |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | 1-2 = Glide                                               |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | 2-1 = Humanitarian Plan                                   |
|                                                                                                                                        +----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
|                                                                                                                                        | @code                | Specifies the code from a particular vocabulary.                                                      |                                                                           |                                                           |
+----------------------------------------------------------------------------------------------------------------------------------------+----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
| `default-aid-type <https://iatistandard.org/activity-standard/iati-activities/iati-activity/default-aid-type>`__                       | @vocabulary          | A `code <https://iatistandard.org/codelists/aidtypevocabulary>`__                                     | Each activity should only contain one code from each aid type vocabulary  | It is recommended that the OECD aid type codes are used.  |
|                                                                                                                                        |                      | for a recognised vocabulary identifying the type of default aid.                                      | (this is to be a rule at the next major upgrade).                         |                                                           |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | Additional humanitarian vocabularies are:                 |
|                                                                                                                                        |                      |                                                                                                       |                                                                           |                                                           |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | 2 = Earmarking category                                   |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | 3 = Earmarking modality                                   |
|                                                                                                                                        |                      |                                                                                                       |                                                                           | 4 = Cash and voucher modalities                           |
|                                                                                                                                        +----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+
|                                                                                                                                        | @code                | Specifies the code from a particular vocabulary.                                                      |                                                                           |                                                           |
+----------------------------------------------------------------------------------------------------------------------------------------+----------------------+-------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------+-----------------------------------------------------------+

Humanitarian elements and attributes to use at transaction level
----------------------------------------------------------------

+------------------------------------------------------------------------------------------------------------------------------------------------+---------------+-------------------------------------------------------------------------------------------------+-----------------------------------------------------+------------------------------------------------------------------------------+
|  Element                                                                                                                                       | Attribute     | Use                                                                                             | Rules                                               | Guidance                                                                     |
+------------------------------------------------------------------------------------------------------------------------------------------------+---------------+-------------------------------------------------------------------------------------------------+-----------------------------------------------------+------------------------------------------------------------------------------+
| `transaction <https://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction>`__                                         | @humanitarian | A flag to indicate that the transaction relates to humanitarian aid.                            |                                                     | If the entire activity relates to humanitarian aid this should be reported   |
|                                                                                                                                                |               |                                                                                                 |                                                     | using iati-activity/@humanitarian, rather than for each transaction.         |
|                                                                                                                                                |               |                                                                                                 |                                                     |                                                                              |
|                                                                                                                                                |               |                                                                                                 |                                                     | Values available:                                                            |
|                                                                                                                                                |               |                                                                                                 |                                                     |                                                                              |
|                                                                                                                                                |               |                                                                                                 |                                                     | 1 = Humanitarian                                                             |
|                                                                                                                                                |               |                                                                                                 |                                                     | 0 = Development                                                              |
+------------------------------------------------------------------------------------------------------------------------------------------------+---------------+-------------------------------------------------------------------------------------------------+-----------------------------------------------------+------------------------------------------------------------------------------+
| `transaction-type <https://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/transaction-type>`__                   | @code         | Specifies the `type <https://iatistandard.org/codelists/transactiontype>`__                     | This must be included once for each transaction.    | Transaction types 12: Outgoing Pledge and 13: Incoming Pledge were added to  |
|                                                                                                                                                |               | of financial transaction e.g. pledge, commitment or disbursement.                               |                                                     | allow the publication of pledges in humanitarian contexts.                   |
+------------------------------------------------------------------------------------------------------------------------------------------------+---------------+-------------------------------------------------------------------------------------------------+-----------------------------------------------------+------------------------------------------------------------------------------+
| `provider-org <https://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/provider-org>`__                           | @type         | Specified the `type <https://iatistandard.org/codelists/organisationtype>`__                    |                                                     | Where possible, in country organisations should be identified.               |
| and `receiver-org <https://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/receiver-org>`__                       |               | of organisation providing or receiving the funds.                                               |                                                     |                                                                              |
+------------------------------------------------------------------------------------------------------------------------------------------------+---------------+-------------------------------------------------------------------------------------------------+-----------------------------------------------------+------------------------------------------------------------------------------+
| `aid-type <https://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/aid-type>`__                                   | @vocabulary   | A `code <https://iatistandard.org/codelists/aidtypevocabulary>`__ for a                         | Each transaction should only contain one code from  | It is recommended that the OECD aid type codes are used.                     |
|                                                                                                                                                |               | recognised vocabulary identifying the type of default aid.                                      | each aid type vocabulary (this is to be a rule at   |                                                                              |
|                                                                                                                                                |               |                                                                                                 | the next major upgrade).                            | Additional humanitarian vocabularies are:                                    |
|                                                                                                                                                |               |                                                                                                 |                                                     |                                                                              |
|                                                                                                                                                |               |                                                                                                 |                                                     | 2 = Earmarking category                                                      |
|                                                                                                                                                |               |                                                                                                 |                                                     | 3 = Earmarking modality                                                      |
|                                                                                                                                                |               |                                                                                                 |                                                     | 4 = Cash and voucher modalities                                              |
|                                                                                                                                                +---------------+-------------------------------------------------------------------------------------------------+-----------------------------------------------------+------------------------------------------------------------------------------+
|                                                                                                                                                | @code         | Specifies the code from a particular vocabulary.                                                |                                                     |                                                                              |
+------------------------------------------------------------------------------------------------------------------------------------------------+---------------+-------------------------------------------------------------------------------------------------+-----------------------------------------------------+------------------------------------------------------------------------------+

Humanitarian reporting should include
-------------------------------------

**Please note:**

When using the IATI Activity Standard to declare humanitarian related activities the following should be considered:

* It is recommended that at least ``iati-activity/@humanitarian`` attribute and the humanitarian-scope element should be used for each humanitarian related activity.
* If an emergency is not defined on any of the lists included on the `Humanitarian Scope Vocabulary <https://iatistandard.org/codelists/humanitarianscopevocabulary>`__ list then a publisher can declare their own values using code ‘99’. It is recommended that the title of an emergency is constructed using the format  [location of event] + [type of event] + [month of event] + [year of event].  For example, ‘Nepal Earthquake April 2015’.

.. meta::
  :title: Humanitarian reporting
  :description: Please read detailed publishing guidance on how to use the humanitarian elements and attributes.
  :guidance_type: activity
  :date: February 17, 2021
