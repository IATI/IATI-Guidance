Financial transactions
======================

Each activity in IATI should contain a record of how the activity is being financed and how the finance is being used. Each incoming and outgoing fund is published as a transaction. Publishers can choose the type of transaction that best reflects the real flow of money in and out of their organisation. This could be incoming commitments (the promise of money) or incoming funds (the actual transfer of money).

Each transaction should specify: the date on which the transaction took place, the value of the transaction, and who gave and received the money. Further details about a transaction can be included by adding :doc:`classifications <activity-classifications>` to each transaction. This includes the type of finance being published, whether or not the finance is for a specific purpose and if there is a specific policy area that the finance will be targeting.

If an organisation makes many small transactions, these can be grouped together. For example, expenses could be published as one transaction for every month or every quarter. When deciding whether to aggregate transactions by month or quarter, it is recommended that publishers consider the needs of likely data users.

Please note, the flow of funds to or from multiple external organisations should **not** be grouped together. Transactions should be linked to the IATI activities published by either the providing or receiving organisation. Such links allow data users to trace the flow of funds between organisations.

**Example**

The example below shows an incoming fund of $8,000 being received by an organisation. The provider’s IATI org ID has been added using the @ref attribute. The activity from which the provider has disbursed the funds has been added using the @provider-activity-id attribute. These details allow a data user to trace the fund up the chain:

.. code-block:: xml

  <transaction>
    <transaction-type code="1" />
    <transaction-date iso-date="2018-06-01" />
    <value currency="USD" value-date="2018-06-01">8000</value>
    <description>
      <narrative>Incoming funds from an external organisation </narrative>
    </description>
    <provider-org provider-activity-id="XI-IATI-1234-activity" type="10" ref="XI-IATI-1234">
      <narrative>Name of the provider</narrative>
    </provider-org>
  </transaction>

Transactions can be positive or negative. An example of a negative transaction would be money that was disbursed to a partner and is then being returned to the funder. The returned funds should be published as a disbursement transaction with a negative value, i.e. with a minus symbol in front of the figure, e.g. -1000.

**Example**
-----------

An organisation has committed $10,000 to an external organisation. Later, this commitment is dropped to $8,000. This should be published as two separate outgoing commitments. One for $10,000, followed by another for -$2,000. Please note: the provider and receiver organisations are missing from this example.

.. code-block:: xml

  <transaction>
    <transaction-type code="2" />
    <transaction-date iso-date="2018-01-01" />
    <value currency="USD" value-date="2018-01-01">10000</value>
  </transaction>
  <transaction>
    <transaction-type code="2" />
    <transaction-date iso-date="2018-06-01" />
    <value currency="USD" value-date="2018-06-01">-2000</value>
  </transaction>

Transactions should include:
----------------------------

Please note:

- Every activity should include at least one transaction.
- A transaction always describes something that has already happened. Therefore, transaction and value dates must not be in the future.
- Each transaction can have a reference, this can be used to link a transaction to the publisher’s internal financial management system.
- IATI recommends that commitments and pledges are followed by the actual movement of money (incoming fund, disbursement or expenditure). For each commitment, there should be a corresponding disbursement on the date when the funds were disbursed.
- Dates should be in the format YYYY-MM-DD, e.g. 2018-03-16.
- Transaction values can contain decimals.
- Transaction values must not contain commas e.g. 3000 is acceptable, 3,000 is not.
- Transaction values can be positive or negative. Where finance is being passed up the delivery chain, this should be published as a negative transaction. E.g. if a grantee was returning $500, the provider should publish a disbursement of -$500 to the grantee.

For each transaction it is strongly recommended that both the **provider** and **receiver organisations** are published. This includes when the `reporting-org <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/reporting-org/>`__ is either the provider or the receiver. To find the organisation ID for an organisation, please check if it is publishing via the `IATI Registry <update link>`__ or search for them using the `org-ID finder <https://org-id-finder.codeforiati.org/>`__.

Technical guidance summary
--------------------------

All organisations should include the elements below when publishing a transaction.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1

   * - Element
     - Use
     - Rules
     - Guidance

   * - `transaction-type <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/transaction-type/>`__
     - Specifies the `type <http://reference.iatistandard.org/codelists/TransactionType/>`__ of financial transaction e.g. pledge, commitment or disbursement.
     - This must be included once and only once for each transaction.
     - It is good practice to publish commitments, followed by the corresponding incoming fund or disbursement.

   * - `transaction-date <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/transaction-date/>`__
     - The specific date on which the transaction took place, or when the commitment or pledge was made.
     - This must be included once and only once for each transaction.

       Transactions must not have future dates at the time of publishing.
     -

   * - `value <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/value/>`__
     - Defines the amount of finance given, as well as the currency it’s published in and the date on which it was valued.
     - This must be included once and only once for each transaction.

       The `currency <http://reference.iatistandard.org/codelists/Currency/>`__ must be published here if a `default-currency <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/>`__ is not included.

       The value-date must be published here and must not be in the future at the time of publishing.
     - The currency code should be given only if it is different from the default-currency provided for the activity.

   * - `description <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/description/>`__
     - A short description of the transaction e.g. what it was for.
     - This must be included once and only once for each transaction.
     - The description text is contained within the child narrative element. This can be repeated in multiple languages.

   * - `provider-org <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/provider-org/>`__
     - The organisation that provided the finance.

       This should include their IATI Org ID, their activity ID if known, and the type of organisation.
     - The element must occur once and only once.

       If the provider-org does not have an IATI Org ID, the name of the organisation must be given.
     - This should be included for all transactions.

       If known, it is strongly recommended to include the provider-org’s activity ID.

       If the provider-org element is missing, it is presumed that the reporting-org is the provider of the funds.

   * - `receiver-org <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/receiver-org/>`__
     - The organisation that received the finance.

       This should include their IATI Org ID, their activity ID if known, and the type of organisation.
     - The element must occur once and only once.

       If the receiver-org does not have an IATI Org ID, the name of the organisation must be given.
     - This should be included for all transactions.

       If known, it is strongly recommended to include the receiver-org’s activity ID.

       If the receiver-org element is missing, it is presumed that the reporting-org is the provider of the funds.

Contextual information
----------------------

Thematic (sector) and geographic (country and region) details can be published either once per activity, or for each transaction. They should be published at the same level. They must not appear at both activity and transaction levels. Please see the :doc:`thematic <activity-thematic-focus>` (sector) and :doc:`geographic <countries-regions>` (country and region) pages for more details.

Further classifications
-----------------------

There are several classifications that can be added to a particular transaction, such as the type of finance and how It is being shared. These values override the default values published at activity level. For information on these classifications, see the :doc:`activity classifications <activity-classifications>` page.

.. meta::
  :title: Financial transactions
  :description: Each activity in IATI should contain a record of how the activity is being financed and how the finance is being used. Each incoming and outgoing fund is published as a transaction.
  :guidance_type: activity
  :date: September 19, 2019
