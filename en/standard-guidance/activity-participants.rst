Activity Participants
======================

In IATI data, each organisation publishes from its own perspective and includes details of organisations it is working with. Each publisher should be publishing the money coming into their organisation and what they are doing with it. The work they do may involve other organisations. These could be organisations from which they are receiving money from, organisations to which they are giving money, or partner organisations.

There are multiple points in Organisation and Activity files that can reference the organisations a publisher is working with. They should be identified by their name, unique IATI organisation ID (referred to as an IATI Org ID) and activity IDs (also referred to as IATI Identifiers). Their role and what type of organisation they are must also be added. For guidance on how to formulate an IATI Org ID see `here <https://iatistandard.org/en/guidance/preparing-organisation/organisation-account/how-to-create-your-iati-organisation-identifier/>`__.

It is useful for data users to know who an organisation is working with, as well as being able to trace the flow of funds up and down the delivery chain. This is enabled by publishers including the unique IATI Org IDs for the external organisations they are working with. IATI Org IDs can be added to activity data by use of the `participating-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/participating-org/>`__ and `transaction <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/>`__ elements. It is always recommended that the IATI Organisation ID is added (if possible) and the organisation’s name.

   The current list of publishers can be found on the `IATI Registry. <https://iatiregistry.org/publisher>`__

Where can activity participants can be published?
------------------------------------------------

**Organisation file:**

Each organisation file must specify which organisation is publishing the file, and which organisation the data is about. In most cases, the publishing organisation is publishing data about itself. The organisation file can also include external organisations to which the publisher is providing core funding.

Please note:

-  In most cases, an organisation file will be from the perspective of one organisation. Guidance on publishing from the perspective of multiple organisations is coming soon.

-  It is always recommended that the IATI Org ID and the organisation’s name is included.

Technical guidance summary
--------------------------

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `organisation-identifier <http://iatistandard.org/organisation-standard/iati-organisations/iati-organisation/organisation-identifier/>`__
     - The IATI organisation ID (Org ID) of the organisation whose data is being published.

       This organisation may be different from the organisation publishing the file.
     - This element must be included once and only once.

       This must be a valid IATI Org ID.

       To publish on behalf of another organisation, the `iati-organisation <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/>`__ element should be repeated.
     -

   * - `name <http://iatistandard.org/organisation-standard/iati-organisations/iati-organisation/name/>`__
     - A (human-readable) name for the organisation whose data is being published.
     - This element must be included once and only once.

       This name can be repeated in different languages.
     -

   * - `reporting-org <http://iatistandard.org/organisation-standard/iati-organisations/iati-organisation/reporting-org/>`__
     - The IATI Org ID of the organisation publishing the data.
     - This element must be included once and only once.

       The @ref attribute must match the IATI Org ID for the organisation on the IATI Registry.

       The `type <http://reference.iatistandard.org/codelists/OrganisationType/>`__ of organisation publishing the file is required.
     - The name of the organisation can be added under the ‘narrative’ element.

   * - `recipient-org <http://iatistandard.org/organisation-standard/iati-organisations/iati-organisation/recipient-org-budget/recipient-org/>`__ (budget)
     - The IATI Org ID and name of the organisation that will be receiving the core funding
     - This element must be included once and only once within each `recipient-org-budget <http://reference.iatistandard.org/203/organisation-standard/iati-organisations/iati-organisation/recipient-org-budget/>`__.

       If the IATI Org ID is not known, the name of the organisation must be given in the narrative.
     - Publishing recipient-org-budget elements is primarily applicable to donors, but any provider of core funding is expected to use it.


**Activity File:**

Activity files need to specify which organisation is publishing the data.

Details of participating organisations, what their roles are and who is receiving and giving the funds can also be published.

Please note:

-  In most cases, an organisation file will be from the perspective of one organisation. Guidance on publishing from the perspective of multiple organisations is coming soon.

-  The role/s of the pub organisation should be provided (e.g. implementing and accountable).

-  Activities can have multiple participating organisations with the same role (e.g. implementing and accountable).

-  A participating organisation can also have multiple roles.

-  It is always recommended that as many details as possible about an organisation which are known are added.

-  For each transaction it is recommended that both the provider and receiver organisations are added, this includes when the reporting organisation is either the provider or the receiver.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1

   * - Element
     - Use
     - Rules
     - Guidance

   * - `reporting-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/reporting-org/>`__
     - The IATI Org ID of the organisation publishing the file.
     - This element must be included once and only once.

       The @ref attribute must match the IATI Org ID for the organisation on the IATI Registry.

       All activities in a file must contain the same @ref attribute.

       A code from the `Organisation Type <http://reference.iatistandard.org/codelists/OrganisationType/>`__ codelist is required.
     - The name of the organisation can be added under the ‘narrative’ element.

   * - `participating-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/participating-org/>`__
     - Specifies which organisations are involved with the activity, and their individual `roles <http://reference.iatistandard.org/codelists/OrganisationRole/>`__ are.
     - If the IATI Org ID for the participating organisation is not known, then their name must be given.

       Participating organisations must be given a role from the `Organisation Role <http://reference.iatistandard.org/codelists/OrganisationRole/>`__ codelist.

       At least one participating organisation must be published.
     - An organisation can play multiple roles (e.g. funding and implementing); in such a case each role should be published, and the name of the organisation repeated.

   * - `provider-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/provider-org/>`__ (transaction)
     - The organisation that provided the finance.

       This should include the organisation’s IATI Org ID, activity ID (if known) and organisation `type <http://reference.iatistandard.org/codelists/OrganisationType/>`__.
     - This element must be included once and only once.

       If the IATI Org ID for the providing organisation is not known, then their name must be given.
     - This should be included for all finances coming in.

       If known, it is strongly recommended to include the provider-org’s activity ID.

       If the provider-org element is missing, it is presumed that the reporting-org is the provider of the funds.

   * - `receiver-org <http://iatistandard.org/activity-standard/iati-activities/iati-activity/transaction/receiver-org/>`__ (transaction)
     - The organisation that received or will receive the funds.

       This should include the organisation’s IATI Org ID, their activity ID (if known) and organisation `type <http://reference.iatistandard.org/codelists/OrganisationType/>`__.
     - This element must be included once and only once.

       If the receiver-org does not have an IATI Org ID, the name of the organisation must be given.
     - This should be included for all finances going out.

       If known it is strongly recommended to include the receiver-org’s activity ID.

       If the receiver-org element is missing, it is presumed that the reporting-org is the provider of the funds.
