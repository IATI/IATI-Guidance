IATI traceability guidance
==========================

The inclusion of specific data within IATI activities allows users to trace the flow of funds from the original donors down to the intended beneficiaries. Delivery chains can be long and complex. For example:

  *Several donors might contribute to a multi-donor trust fund, which contracts a series of international NGOs, who in turn use local NGO partners, who then hire local contractors to deliver services.*


.. image:: media/traceability_diagram_1.png
   :width: 13.901in
   :height: 3.69in

Each organisation needs to publish to IATI and link their data with their partners. Publishers should include who they are giving funding to, and who they are receiving funding from. They should also include references to the related activities their partners have published. As each activity has a unique IATI Activity Identifier, this identifier can be referenced by partner organisations.
   
When all publishers include the unique IATI Activity Identifier in their publishing, data users can identify the related activities, find partners working on the same activity and track the flow of funds both up and down the delivery chain. This is traceability. For example:


  *If Organisation A gives Organisation B £500 as part of their activity A1, Organisation B should publish a receipt of the £500 from Organisation A. Organisation B should include a reference to activity A1, showing the activity their funding came from. This allows data users to track the flow of funds through the delivery chain.*

.. image:: media/traceability_diagram_2.png
   :width: 13.901in
   :height: 3.69in

Achieving traceability across all IATI data requires every publisher to include data on the organisation(s) and activity(s) from which their funding is coming from and, where possible, going to.

Types of identifiers
--------------------

Each organisation publishing to IATI will have:

- `IATI Organisation Identifier <https://iatistandard.org/en/guidance/publishing-data/registering-and-managing-your-organisation-account/how-to-create-your-iati-organisation-identifier/>`__
  
  This is a unique identifier for their organisation e.g. `XM-DAC-41114 <http://d-portal.org/ctrack.html?reporting_ref=XM-DAC-41114#view=main/>`__ for the United Nations Development Programme (UNDP). View the list of all IATI Organisation Identifiers `here <https://www.iatiregistry.org/publisher>`__

- `IATI Activity Identifier <https://iatistandard.org/en/guidance/standard-overview/preparing-your-data/activity-information/creating-iati-identifiers/>`__
  
  Every IATI activity has a unique identifier. This is formed of the publishing organisation’s IATI Organisation Identifier followed by a unique code e.g. XM-DAC-41114`-OUTPUT-00114444 <http://d-portal.org/ctrack.html?reporting_ref=XM-DAC-41114#view=act&aid=XM-DAC-41114-OUTPUT-00114444>`__

Using identifiers
-----------------

If you are receiving funds from an organisation already publishing to IATI, you are expected to include their IATI Organisation Identifier and the unique IATI Activity Identifier from which they are providing the funds.

If you are providing funds to a downstream partner, the IATI Organisation Identifier for this organisation should also be included. If the partner organisation is not yet publishing to IATI, you should just include their name.

1) **Include the participating organisations**
  
  Each organisation involved in the activity (funding, accountable, extending or implementing) should be listed. 

  The level of detail for each participating organisation will depend on where in the network they are or also any confidentiality concerns. You should provide as much information as possible from the full list below that is available to you at the time of publishing:

  - Name
  - Organisation `type <https://iatistandard.org/en/iati-standard/203/codelists/organisationtype/>`__ 
  - Organisation `role <https://iatistandard.org/en/iati-standard/203/codelists/organisationrole/>`__
  - IATI Organisation Identifier (if known)
  - Unique IATI Activity Identifier (if known)

  Reporting organisations can play different roles. 

2) **Add transaction provider and receiver organisations**

  Activity :doc:`transactions <financial-transactions>` show how an activity is being financed:

  - **Incoming transactions:** commitments (the promise of money) and incoming funds (the actual transfer of money). These originate from an external organisation.
  - **Outgoing transactions:** commitments (promise of money) and disbursements (actual transfer of money). These funds are going to an external organisation. 

  Use your list of participating organisations to add details of the `provider-org <http://iatistandard.org/203/activity-standard/iati-activities/iati-activity/transaction/provider-org/>`__ and `receiver-org <http://iatistandard.org/203/activity-standard/iati-activities/iati-activity/transaction/receiver-org/>`__ for each transaction. For incoming transactions, there should be an external provider and the reporting-org is the receiver. For outgoing transactions, the reporting-org is the provider and an external organisation is the receiver-org.

  You should provide as much of the information listed below as possible that is available to you at the time of publishing:

  - Name
  - Organisation `type <https://iatistandard.org/en/iati-standard/202/codelists/organisationtype/>`__ 
  - IATI Organisation Identifier @ref (if known)
  - Unique IATI Activity Identifier @provider-activity-id or @receiver-activity-id (if known)

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Code
     - Name
     - Inclusion of external provider or receiver organisation
     - Incoming or outgoing transactions (this would help you in understanding if provider or receiver should be included)

   * - 1
     - Incoming Funds
     - Provider organisation
     - Incoming flow

   * - 2
     - Outgoing Commitment
     - Receiver organisation
     - Outgoing flow

   * - 3
     - Disbursement
     - Receiver organisation
     - Outgoing flow

   * - 4
     - Expenditure
     - N/A
     - Outgoing flow

   * - 5
     - Interest Payment
     - Receiver organisation
     - Outgoing flow

   * - 6
     - Loan Repayment
     - Receiver organisation
     - Outgoing flow

   * - 7
     - Reimbursement
     - Receiver organisation
     - Outgoing flow

   * - 8
     - Purchase of Equity
     - Receiver organisation
     - Outgoing flow     

   * - 9
     - Sale of Equity
     - Provider organisation
     - Incoming flow

   * - 10
     - Credit Guarantee
     - Receiver organisation
     - Outgoing flow

   * - 11
     - Incoming Commitment
     - Provider organisation
     - Incoming flow

   * - 12
     - Outgoing Pledge
     - Receiver organisation
     - Outgoing flow

   * - 13
     - Incoming Pledge
     - Provider organisation
     - Incoming flow
     


3) **Include your parent and child activities**

  If an activity is part of a ‘programme with multiple activities’ within a single organisation, the related programme/parent and sub-activities/children should be listed using the `related-activity <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/related-activity/>`__ element. 

  Details to include:
  - Unique IATI Activity Identifier (`@ref <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/related-activity/>`__)
  - Related activity `type <https://iatistandard.org/en/iati-standard/203/codelists/relatedactivitytype/>`__ of relationship (e.g. 1: parent,  2: child, 3: sibling).

.. meta::
  :title: IATI traceability guidance
  :description: The inclusion of specific data within IATI activities allows users to trace the flow of funds from the original donors down to the intended beneficiaries.
  :guidance_type: activity
  :date: June 07, 2021
