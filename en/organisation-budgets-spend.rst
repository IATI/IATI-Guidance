Organisation budgets and spend
==============================

An organisation budget is a total planned budget for an organisation for a given time period, and these can be broken down into different programmes or areas of work. These budgets are published in organisation files. IATI recommends that organisation files contain budgets for the next three fiscal years.

Similar to an annual report, the `total-budget <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/>`__ element covers all of an organisation’s expected development and humanitarian spend for the current and following three years. Each budget must span a period of no more than 12 months, preferably aligned with the publishing organisation’s fiscal year.

Budgets can also be published for intervals or timeframes of less than one year. For example, it can be helpful for budgets to be broken down into quarters to help recipient countries match the budgets to their own fiscal years. The time periods of the budgets should not overlap. This means that a user should be able to add up all the values an organisation is publishing in their total-budget elements to get a total budget for that timeframe.

IATI strongly encourages organisations to break down their total budget into smaller budgets for the recipient `countries <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/recipient-country-budget/>`__ and recipient `regions <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/recipient-region-budget/>`__ in which they operate. Budgets for planned core funding to `recipient organisations <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/recipient-org-budget/>`__ (where applicable) can also be published. These budgets can overlap between the three different budget elements, but there should be no duplication within each.

Please note that the same budget should not be published in multiple currencies.


**For example**

- An organisation has a budget of $2,000 for the year 2020.

- This funding is being split equally between Uganda and Kenya.

- The reporting organisation has committed $500 of the budget to be core funding for organisation 1 to carry out some of the work.

  **Total Budget**

.. code-block:: xml

  <total-budget status="1">
    <period-start iso-date="2020-01-01" />
    <period-end iso-date="2020-12-31" />
    <value value-date="2020-01-01">2000</value>
  </total-budget>

**Recipient Org Budget**

.. code-block:: xml

  <recipient-org-budget status="2">
    <recipient-org ref="org-1" />
    <period-start iso-date="2020-01-01" />
    <period-end iso-date="2020-12-31" />
    <value value-date="2020-01-01">500</value>
  </recipient-org-budget>

**Recipient Country Budget - Uganda**

.. code-block:: xml

  <recipient-country-budget status="1">
    <recipient-country code="UG" />
    <period-start iso-date="2020-01-01" />
    <period-end iso-date="2020-12-31" />
    <value value-date="2020-01-01">1000</value>
  </recipient-country-budget>

**Recipient Country Budget - Kenya**

.. code-block:: xml

  <recipient-country-budget status="1">
    <recipient-country code="KE" />
    <period-start iso-date="2014-01-01" />
    <period-end iso-date="2014-12-31" />
    <value value-date="2020-01-01">1000</value>
  </recipient-country-budget>

When publishing a budget for a recipient country, the budget periods should match the fiscal year for the specific country. This is in order to help the recipient of the funds with their budgeting. The budgets can also be published in the currency of the recipient country. This is shown by using the `currency <http://reference.iatistandard.org/codelists/Currency/>`__ attribute to override the default publishing currency of the reporting organisation. Please note that the same budget should not be published in multiple currencies.

Budgets often change over time. When this happens, the budget value and corresponding data should be amended. Each budget can have one of two status codes, either:

-  **indicative (1)** - a non-binding estimate for the described budget.
-  **committed (2)** - a binding agreement for the described budget.

When a budget changes status, the value and budget `status <http://reference.iatistandard.org/codelists/BudgetStatus/>`__ already in the file should be amended. A new budget should not be created.

What should organisation budgets include?
-----------------------------------------

Please note:

-  Each budget should be described from the perspective of the reporting organisation.

-  Budget values should not be negative.

-  Budgets can be updated at any point. When a budget changes, this budget value and status should be amended. A new budget element should not be created.

-  The budget `status <http://reference.iatistandard.org/codelists/BudgetStatus/>`__ explains whether the budget being published is indicative or has been formally committed.

-  If no status is present, the budget is assumed to be indicative.

-  Budgets must be published in periods of no longer than a year.

-  The `total-budget <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/>`__ in an organisation file is the total amount the organisation plans to spend on humanitarian and development work across the given time period.

-  The periods published within the total-budget element should not overlap.

-  Total-budgets should be published according to the fiscal year of the reporting organisation.

-  The total budget can be broken down into budgets for recipient countries, regions and organisations.

-  Recipient country budgets should be presented according to the fiscal years or planning cycle of the recipient country.

-  Recipient country budgets can be published in the currency of the country. However, budget values should not be repeated in multiple currencies.

-  The sum of budget lines, or budget breakdowns, does not have to equal the overall value provided for recipient country, region, organisation or total budgets.

Technical guidance summary
--------------------------

**Organisation budget information**

All organisations should include the elements below to publish their annual planned budgets:

+----------------+----------------+----------------+----------------+
| Element        | Use            | Rules          | Guidance       |
+================+================+================+================+
| `total-budget  | This provides  |                | The            |
| <http://refere | the            |                | organisation’s |
| nce.iatistanda | organisation’s |                | total annual   |
| rd.org/organis | own budget for |                | planned budget |
| ation-standard | humanitarian   |                | for the next   |
| /iati-organisa | and            |                | three years    |
| tions/iati-org | development    |                | should be      |
| anisation/tota | work for the   |                | provided.      |
| l-budget/>`__  | following      |                |                |
|                | period.        |                | If the         |
|                |                |                | `status <http: |
|                | The            |                | //reference.ia |
|                | `status <http: |                | tistandard.org |
|                | //reference.ia |                | /codelists/Bud |
|                | tistandard.org |                | getStatus/>`__ |
|                | /codelists/Bud |                | attribute is   |
|                | getStatus/>`__ |                | not declared,  |
|                | attribute can  |                | the budget is  |
|                | be declared to |                | assumed to be  |
|                | say if the     |                | indicative.    |
|                | budget is      |                |                |
|                | indicative or  |                |                |
|                | formally       |                |                |
|                | committed.     |                |                |
+----------------+----------------+----------------+----------------+
| `period-start  | An iso-code    | The elements   | The periods    |
| <http://refere | for the start  | period-start   | should align   |
| nce.iatistanda | date of the    | and period-end | with the       |
| rd.org/organis | budget.        | must appear    | fiscal year of |
| ation-standard |                | only once      | the reporting  |
| /iati-organisa |                | within each    | organisation.  |
| tions/iati-org |                | budget         |                |
| anisation/tota |                | element.       |                |
| l-budget/perio |                |                |                |
| d-start/>`__   |                | The            |                |
|                |                | period-start   |                |
|                |                | date must be   |                |
|                |                | before or the  |                |
|                |                | same as the    |                |
|                |                | period-end     |                |
|                |                | date.          |                |
|                |                |                |                |
|                |                | The period     |                |
|                |                | reported must  |                |
|                |                | be no longer   |                |
|                |                | than one year. |                |
+----------------+----------------+                +----------------+
| `period-end    | An iso-code    |                |                |
| <http://refere | for the end    |                |                |
| nce.iatistanda | date of the    |                |                |
| rd.org/organis | budget.        |                |                |
| ation-standard |                |                |                |
| /iati-organisa |                |                |                |
| tions/iati-org |                |                |                |
| anisation/tota |                |                |                |
| l-budget/perio |                |                |                |
| d-end/>`__     |                |                |                |
+----------------+----------------+----------------+----------------+
| `value <http   | The financial  | This element   | The currency   |
| ://reference.i | value of the   | must appear    | attribute is   |
| atistandard.or | budget for the | only once      | required,      |
| g/organisation | declared       | within each    | unless a       |
| -standard/iati | period.        | budget         | default        |
| -organisations |                | element.       | currency has   |
| /iati-organisa | The            |                | been provided  |
| tion/total-bud | `currency <h   | The value      | for the        |
| get/value/>`__ | ttp://referenc | declared must  | organisation.  |
|                | e.iatistandard | be an integer. |                |
|                | .org/codelists |                |                |
|                | /Currency/>`__ | The value-date |                |
|                | and value-date | must be        |                |
|                | can also be    | declared for   |                |
|                | declared for   | the value.     |                |
|                | the value.     |                |                |
+----------------+----------------+----------------+----------------+

**Budget lines**

Further budget information can be added by using the budget-line element. Budget lines allow the total-budget element to be broken down into sub-budgets and a description added, such as budget breakdowns and descriptions for different programmes happening in a given year.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `budget-line <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/budget-line/>`__
     - This provides a breakdown of the total-budget.

       The period covered is the same as that of the parent total-budget.

       Multiple budget-lines can be published.
     -
     - The sum of the budget-line values does not have to equal the value of the parent total-budget element.

       An @ref attribute can be provided, linking the budget-line to an internal reference taken from the reporting organisation’s system.

   * - `value <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/budget-line/value/>`__
     - The value of the budget-line breakdown.
     - This element must appear once and only once within each budget-line element.

       The value-date must be declared for the value.
     -

   * - `narrative <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/budget-line/narrative/>`__
     - A description of the budget-line breakdown.
     - A narrative must be provided.
     - The description text is within the child narrative element.

       This can be repeated in multiple languages.


**Additional budget breakdown**

Three other breakdowns of the total-budget can be provided. These are by `recipient organisation <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/recipient-org-budget/>`__, `recipient country <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/recipient-country-budget/>`__ and as of v2.02 `recipient region <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/recipient-region-budget/>`__. These allow publishers to provide forward-looking budgets for each organisation they plan to disburse money to, plus the countries and regions they are operating in.

IATI recommends that, where possible, recipient country budget periods should align with the recipient country’s budgetary or planning cycle.

Each budget breakdown does not have to use the same budget periods. Nor do these budgets have to add up to the organisation’s total budget.

The three budget breakdowns listed above contain the same structure and sub-elements as the total-budget. However, they additionally declare the recipient organisation, country or region.

**Organisation total expenditure**

Once an organisation knows their total spend for a budget period, as declared in the `total-budget <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/>`__ elements, IATI recommends that this too is published. This can be done through the `total-expenditure <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-expenditure/>`__ element. This allows users to work out ‘coverage’ – the percentage of an organisation’s total spend captured in its published IATI activities. IATI recommends that all IATI publishers include this data for the previous three years.

Total expenditure is defined as the total amount of humanitarian and development disbursement and expenditure an organisation has made in a given time period.

Like budget-lines, the total expenditure can be broken down into expense-lines.

+----------------+----------------+----------------+----------------+
| Element        | Use            | Rules          | Guidance       |
+----------------+----------------+----------------+----------------+
| `total-expendi | This provides  |                | The            |
| ture <http://r | the            |                | organisation’s |
| eference.iatis | organisation’s |                | total          |
| tandard.org//o | own            |                | expenditure    |
| rganisation-st | humanitarian   |                | for the        |
| andard/iati-or | and            |                | previous three |
| ganisations/ia | development    |                | years should   |
| ti-organisatio | spend for the  |                | be provided.   |
| n/total-expend | following      |                |                |
| iture/>`__     | period.        |                |                |
+----------------+----------------+----------------+----------------+
| `period-start  | An iso-code    | The elements   | The periods    |
| <http://refere | for the start  | period-start   | should align   |
| nce.iatistanda | date of the    | and period-end | with the       |
| rd.org/organis | period.        | must appear    | periods        |
| ation-standard |                | only once      | reported in    |
| /iati-organisa |                | within each    | the            |
| tions/iati-org |                | total-expendit | `total-budget  |
| anisation/tota |                | ure element.   |  <http://refer |
| l-expenditure/ |                |                | ence.iatistand |
| period-start/> |                | The            | ard.org/organi |
| `__            |                | period-start   | sation-standar |
|                |                | date must be   | d/iati-organis |
|                |                | before or the  | ations/iati-or |
|                |                | same as the    | ganisation/tot |
|                |                | period-end     | al-budget/>`__ |
|                |                | date.          | element.       |
+----------------+----------------+                +----------------+
| `period-end <h | An iso-code    | The period     |                |
| ttp://referenc | for the end    | published must |                |
| e.iatistandard | date of the    | be no longer   |                |
| .org/organisat | period.        | than one year. |                |
| ion-standard/i |                |                |                |
| ati-organisati |                |                |                |
| ons/iati-organ |                |                |                |
| isation/total- |                |                |                |
| expenditure/pe |                |                |                |
| riod-end/>`__  |                |                |                |
+----------------+----------------+----------------+----------------+
| `value <http:/ | The financial  | This element   | The currency   |
| /reference.iat | value of the   | must appear    | attribute is   |
| istandard.org/ | expenditure    | only once      | required,      |
| organisation-s | for the        | within each    | unless a       |
| tandard/iati-o | declared       | `total-exp     | default        |
| rganisations/i | period.        | enditure <http | currency has   |
| ati-organisati |                | ://reference.i | been provided  |
| on/total-expen | The `currency  | atistandard.or | for the        |
| diture/value/> | <http://refere | g//organisatio | organisation.  |
| `__            | nce.iatistanda | n-standard/iat |                |
|                | rd.org/codelis | i-organisation |                |
|                | ts/Currency/>` | s/iati-organis |                |
|                | __ and         | ation/total-ex |                |
|                | value-date can | penditure/>`__ |                |
|                | also be        | element.       |                |
|                | declared for   |                |                |
|                | the value.     | The value-date |                |
|                |                | must be        |                |
|                |                | declared for   |                |
|                |                | the value.     |                |
+----------------+----------------+----------------+----------------+
| `expense-line  | This provides  |                | The sum of the |
| <http://refere | a breakdown of |                | expense-line   |
| nce.iatistanda | the            |                | values does    |
| rd.org/organis | total-expendit |                | not have to    |
| ation-standard | ure.           |                | equal the      |
| /iati-organisa |                |                | value of the   |
| tions/iati-org | The period     |                | parent         |
| anisation/tota | covered is the |                | total-expendit |
| l-expenditure/ | same as that   |                | ure element.   |
| expense-line/> | of the parent  |                |                |
| `__            | total-expendit |                | A @ref         |
|                | ure.           |                | attribute can  |
|                |                |                | be provided    |
|                | Multiple       |                | linking the    |
|                | expense-lines  |                | expense-line   |
|                | can be         |                | to an internal |
|                | published.     |                | reference      |
|                |                |                | taken from the |
|                |                |                | reporting      |
|                |                |                | organisation’s |
|                |                |                | system.        |
+----------------+----------------+----------------+----------------+
| `value <http:/ | The value of   | This element   |                |
| /reference.iat | the            | must appear    |                |
| istandard.org/ | expense-line   | only once      |                |
| organisation-s | breakdown.     | within each    |                |
| tandard/iati-o |                | expense-line   |                |
| rganisations/i |                | element.       |                |
| ati-organisati |                |                |                |
| on/total-expen |                | The value-date |                |
| diture/expense |                | must be        |                |
| -line/value/>` |                | declared for   |                |
| __             |                | the value.     |                |
+----------------+----------------+----------------+----------------+
| `narrative <ht | A description  | A narrative    | The            |
| tp://reference | of the         | must be        | description    |
| .iatistandard. | expense-line   | provided.      | text is        |
| org/organisati | breakdown.     |                | contained      |
| on-standard/ia |                |                | within the     |
| ti-organisatio |                |                | child          |
| ns/iati-organi |                |                | narrative      |
| sation/total-e |                |                | element. This  |
| xpenditure/exp |                |                | can be         |
| ense-line/narr |                |                | repeated in    |
| ative/>`__     |                |                | multiple       |
|                |                |                | languages.     |
+----------------+----------------+----------------+----------------+

Activity budgets
----------------

For details on activity budgets, please see:
- :doc:`Budgets overview <budgets-overview>`
- :doc:`Activity budgets <activity-budgets>`

.. meta::
  :title: Organisation budgets and spend
  :description: An organisation budget is a total planned budget for an organisation for a given time period, and these can be broken down into different programmes or areas of work.
  :guidance_type: organisation
