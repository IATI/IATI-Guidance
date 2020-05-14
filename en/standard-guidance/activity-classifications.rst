Additional activity classifications
===================================

There are many kinds of humanitarian and development financing, each of these can be classified. Funding can come in different `finance types <http://reference.iatistandard.org/codelists/FinanceType/>`__ (including grants, loans, bonds) and `aid types <http://reference.iatistandard.org/codelists/AidTypeVocabulary/>`__ (such as specific project support, core support, pooled funding). It can also come from different types of donors (e.g. as official development assistance from governments, or private development finance from development banks or philanthropic foundations). Organisations publishing data may also want to specify whether an activity or transaction concerns a particular policy area, such as gender equality or disability.

Using the IATI Standard, publishers can assign different classifications to their data. These help users to understand what type of financing it is and how it can be used. As money flows from one organisation to another, these classifications might change. For example, finance from a donor may be untied, then later become tied to a specific purpose as it flows down through multiple implementing partners.

The classification categories used in IATI are aligned, where possible, with those used by other internationally recognised data standards or initiatives, such as the `OECD DAC <https://www.oecd.org/dac/>`__ and the `Grand Bargain <https://www.agendaforhumanity.org/initiatives/3861>`__.

Please note that all classifications in IATI are optional. Activities should include only classifications that are relevant. Some donors require their grantees to publish certain classifications in their activities.

Classifications covered in IATI include:

-  `Aid-type <http://reference.iatistandard.org/codelists/AidTypeVocabulary/>`__

-  `Collaboration-type <http://reference.iatistandard.org/codelists/CollaborationType/>`__

-  `Disbursement-channel <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/disbursement-channel/>`__

-  `Finance-type <http://reference.iatistandard.org/codelists/FinanceType/>`__

-  `Flow-type <http://reference.iatistandard.org/codelists/FlowType/>`__

-  `Policy-marker <http://reference.iatistandard.org/codelists/PolicyMarkerVocabulary/>`__

-  `Tied-status <http://reference.iatistandard.org/codelists/TiedStatus/>`__

What classification information can be published?
-------------------------------------------------

Please note:

-  An activity can have multiple policy-marker attributes. Unlike the element `sector <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/sector/>`__, percentages do not need to be added to each policy-marker.

-  The classifications of default-finance-type, default-flow-type, default-aid-type and default-tied-status apply to the whole IATI-activity. These can be overridden within a single transaction.

-  If an entire activity is wholly tied, partially tied or untied, it is recommended the appropriate default-tied-status code is used.

-  When used at transaction level, tied-status should be published for outgoing and incoming commitments only.

-  If an iati-activity has more than one tied status it is recommended that the published commitment(s) are split into the relevant tied, untied and/or partially-tied amounts and tied-status is published at transaction level.

-  All IATI classifications are optional. Not all classifications may be applicable to an activity.

Technical guidance summary
--------------------------

Classifications that cover the whole activity:

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `policy-marker <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/policy-marker/>`__
     - A policy or theme addressed by the activity.
     - The `significance <http://reference.iatistandard.org/codelists/PolicySignificance/>`__ attribute must be present if OECD `policy marker <http://reference.iatistandard.org/codelists/PolicyMarker/>`__ codes are used.
     - It is recommended that the OECD `policy marker <http://reference.iatistandard.org/codelists/PolicyMarker/>`__ codes are used, codes from additional vocabularies can also be added

       If no codelist is declared, the OECD `policy marker <http://reference.iatistandard.org/codelists/PolicyMarker/>`__ codelist is presumed.

       If vocabulary 99 (reporting-org) is used, a link to the codelist using the @vocabulary-uri attribute should be included; there must also be a description of the code in the `narrative <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/policy-marker/narrative/>`__ element. This helps ensure that users can understand the meaning of the code.

   * - `collaboration-type <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/collaboration-type/>`__
     - Describes what type of organisation is providing the funds (e.g. bilateral or multilateral).
     - This element must be published no more than once.
     -

   * - `default-flow-type <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/default-flow-type/>`__
     - DAC/CRS distinction between ODA (official development assistance) and other types of resource flow.
     - This element must be published no more than once.
     -

   * - `default-finance-type <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/default-finance-type/>`__
     - DAC/CRS distinction between ODA (official development assistance) and other types of resource flow.
     - This element must be published no more than once.
     -

   * - `default-aid-type <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/default-aid-type/>`__
     - The type of aid being supplied (e.g. project-type intervention, budget support or debt relief).
     -
     - It is recommended that the OECD `aid type <http://reference.iatistandard.org/codelists/AidType/>`__ codes are used, codes from additional vocabularies can also be added.

       If no vocabulary is declared, OECD aid type is presumed.

       Each activity should only contain one code from each `aid type vocabulary <http://reference.iatistandard.org/codelists/AidTypeVocabulary/>`__.

   * - `default-tied-status <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/default-tied-status/>`__
     - Specifies where the activity’s commitments are untied, tied, or partially tied.
     - This element must be published no more than once.
     - If an activity’s commitments are a combination of tied, partially tied or untied, it is recommended that tied, partially tied and untied commitments are published as separate transactions and classified with their tied-status.

Classifications can also be added to individual `transactions <https://drive.google.com/open?id=1E3hztk6gWTW5DypLELeSwW5X-Ahg0yjm>`__, these values override the default value published at activity level:

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance


   * - `flow-type <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/flow-type/>`__
     - Optional element to override the top-level default-flow-type element on a transaction-by-transaction basis, if needed.
     - This element must be published no more than once.
     -

   * - `finance-type <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/finance-type/>`__
     - Optional element to override the top-level default-finance-type element on a transaction-by-transaction basis, if needed.
     - This element must be published no more than once.
     -

   * - `aid-type <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/aid-type/>`__
     - Optional element to override the top-level default-aid-type elements on a transaction-by-transaction basis, if needed.
     -
     - It is recommended that the OECD `aid type <http://reference.iatistandard.org/codelists/AidType/>`__ codes are used, codes from additional vocabularies can also be added.

       If no vocabulary is declared, OECD aid type is presumed.

       Each transaction should only contain one code from each `aid type vocabulary <http://reference.iatistandard.org/codelists/AidTypeVocabulary/>`__.

   * - `tied-status <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/tied-status/>`__
     - Optional element to override the top-level default-tied-type element on a transaction-by-transaction basis, if needed.
     - This element must be published no more than once.
     - When used at transaction level, tied-status should be published for outgoing and incoming commitments only.


The disbursement channel can only be added to transactions, it cannot be defined at activity level:

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance


   * - `disbursement-channel <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/disbursement-channel/>`__
     - This describes how the finance is given
     - The code must be present on the `disbursement channel <http://iatistandard.org/codelists/DisbursementChannel/>`__ codelist.

       This element must only be published once for each transaction.
     -
.. meta::
  :title: Additional activity classifications
  :description: Using the IATI Standard, publishers can assign different classifications to their data. These help users to understand what type of financing it is and how it can be used.
  :guidance_type: activity
