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

.. list-table::
   :widths: 50 50
   :header-rows: 1


   * - Total Budget
     - Recipient Org Budget

   * - <**total-budget status**\ ="1">

         <**period-start** iso-date="2020-01-01" />

         <**period-end** iso-date="2020-12-31" />

         <**value** value-date="2020-01-01">2000</\ **value**>


       </**total-budget**\ >
     - <**recipient-org-budget** status="2">

         <**recipient-org** ref="org-1" />

         <**period-start** iso-date="2020-01-01" />

         <**period-end** iso-date="2020-12-31" />

         <**value** value-date="2020-01-01">500</\ **value**>

       </**recipient-org-budget**>

.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Recipient Country Budget - Uganda
     - Recipient Country Budget - Kenya

   * - <**recipient-country-budget** status="1">

         <**recipient-country** code="UG" />

         <**period-start** iso-date="2020-01-01" />

         <**period-end** iso-date="2020-12-31" />

         <**value** value-date="2020-01-01">1000</\ **value**>

       </**recipient-country-budget**>

     - <**recipient-country-budget** status="1">

         <**recipient-country** code="KE" />

         <**period-start** iso-date="2014-01-01" />

         <**period-end** iso-date="2014-12-31" />

         <**value** value-date="2020-01-01">1000</\ **value**>

       </**recipient-country-budget**>


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

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `total-budget <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/>`__
     - This provides the organisation’s own budget for humanitarian and development work for the following period.

       The `status <http://reference.iatistandard.org/codelists/BudgetStatus/>`__ attribute can be declared to say if the budget is indicative or formally committed.
     -
     - The organisation’s total annual planned budget for the next three years should be provided.

       If the `status <http://reference.iatistandard.org/codelists/BudgetStatus/>`__ attribute is not declared, the budget is assumed to be indicative.

   * - `period-start <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/period-start/>`__
     - An iso-code for the start date of the budget.
     - The elements period-start and period-end must appear once and only once within each budget element.

       The period-start date must be before or the same as the period-end date.

       The period published must be no longer than one year.
     - The periods should align with the fiscal year of the reporting organisation.

   * - `period-end <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/period-end/>`__
     - An iso-code for the end date of the budget.
     -
     -

   * - `value <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/value/>`__
     - The financial value of the budget for the declared period.

       The `currency <http://reference.iatistandard.org/codelists/Currency/>`__ and value-date can also be declared for the value.
     - This element must appear once and only once within each budget element.

       The value declared must be an integer.

       The value-date must be declared for the value.
     - The currency attribute is required, unless a default currency has been provided for the organisation.


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

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `total-expenditure <http://reference.iatistandard.org//organisation-standard/iati-organisations/iati-organisation/total-expenditure/>`__
     - This provides the organisation’s own humanitarian and development spend for the following period.
     -
     - The organisation’s total expenditure for the previous three years should be provided.

   * - `period-start <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-expenditure/period-start/>`__
     - An iso-code for the start date of the period.
     - The elements period-start and period-end must appear once and only once within each total-expenditure element.

       The period-start date must be before or the same as the period-end date.

       The period published must be no longer than one year.
     - The periods should align with the periods published in the `total-budget <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-budget/>`__ element.

   * - `period-end <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-expenditure/period-end/>`__
     - An iso-code for the end date of the period.
     -
     -

   * - `value <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-expenditure/value/>`__
     - The financial value of the expenditure for the declared period.

       The `currency <http://reference.iatistandard.org/codelists/Currency/>`__ and value-date can also be declared for the value.
     - This element must appear once and only once within each `total-expenditure <http://reference.iatistandard.org//organisation-standard/iati-organisations/iati-organisation/total-expenditure/>`__ element.

       The value-date must be declared for the value.
     - The currency attribute is required, unless a default currency has been provided for the organisation.

   * - `expense-line <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-expenditure/expense-line/>`__
     - This provides a breakdown of the total-expenditure.

       The period covered is the same as that of the parent total-expenditure.

       Multiple expense-lines can be published.
     -
     - The sum of the expense-line values does not have to equal the value of the parent total-expenditure element.

       An @ref attribute can be provided linking the expense-line to an internal reference taken from the reporting organisation’s system.

   * - `value <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-expenditure/expense-line/value/>`__
     - The value of the expense-line breakdown.
     - This element must appear once and only once within each expense-line element.

       The value-date must be declared for the value.
     -

   * - `narrative <http://reference.iatistandard.org/organisation-standard/iati-organisations/iati-organisation/total-expenditure/expense-line/narrative/>`__
     - A description of the expense-line breakdown.
     - A narrative must be provided.
     - The description text is contained within the child narrative element.

       This can be repeated in multiple languages.
