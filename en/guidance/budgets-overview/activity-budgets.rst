Activity budgets
================

It is recommended that each activity with planned spending that is published to IATI includes one or more budgets. These budgets form the total funding expected to be spent as part of the activity. This allows data users to track the activity budget against the declared spend, to understand the stage of the activity.

  *If an activity **does not** expect to have any spend (disbursements or expenditure), **and** spend is being published in a sub-activity, then a budget figure should not be provided.*

Activity budgets should be added as soon as possible. They can then be updated over time as more or less funding comes in, or the scope of the activity changes.

If an activity spans multiple years, then the budget needs to be broken down into separate years or periods. No budget must span more than 12 months. To aid data use, budgets should be broken down into quarters with the declared time periods being relevant to the reporting organisation or life cycle of the activity.

Exceptions (what to do if a budget can’t be published)
------------------------------------------------------

For some organisations, such as development finance institutions and those working in emergency situations it is not always possible to publish a budget for an activity. Or, an organisation may have other commercial or legal reasons why it cannot publish this data.

In this case the attribute `@budget-not-provided <http://reference.iatistandard.org/codelists/BudgetNotProvided/>`__ (which was added at version 2.03) should be used. The attribute explains why a budget cannot be provided. This should only be used for activities in which a budget is expected i.e. those with expected or actual spend.

Publishing budget changes
-------------------------

**Budget element**

When an activity budget is first published it will likely have the @type attribute code ‘original’ (1). If the budget value is later amended, this should be detailed by adding a new budget element containing the new value and @type code ‘revised’ (2). The new revised figure should be added, rather than the difference from the original to the revised budget. Further changes to the budget should be added by changing the value in the ‘revised’ budget element, and not by adding multiple ‘revised’ budgets for the same time period.

A budget can have one of two status codes, either:

-  **indicative (1):** a non-binding estimate for the described budget.

-  **committed (2):** a binding agreement for the described budget.

When a budget changes `status <http://reference.iatistandard.org/codelists/BudgetStatus/>`__, the status of the existing budget element should change. A new budget element should **not** be created.

To calculate the total budget for an activity, a data user should be able to add up all the revised budget values for different time periods. If some time periods do not have a revised budget, then the original budget should be used for these periods.

**Transaction element**

While budget elements hold the overall budget amounts for an activity, budget fluctuations should be recorded through outgoing commitment `transactions <https://drive.google.com/open?id=1E3hztk6gWTW5DypLELeSwW5X-Ahg0yjm>`__.

*Commitment Transactions*

A budget can either be ‘committed’ (has a binding agreement for the described budget) or ‘indicative’ (is a non-binding estimate for the described budget).

When a budget is committed, the value of the outgoing commitment should be detailed in a transaction. Any changes to the budget, and therefore the outgoing commitment, should be detailed by adding positive and negative outgoing commitment transactions along with the date when the change happened.

This allows data users to sum all of the outgoing commitments to calculate the total amount.

Example usage
-------------

An activity lasts a year. The original budget was $10,000 and was later decreased by $2,000. The final total budget for the activity is $8,000. This should be published as one budget with an ‘original’ status and one with a ‘revised’ status, and two corresponding outgoing commitment transactions.

.. code-block:: xml

<budget type="1" status="2">
  <period-start iso-date="2018-01-01" />
  <period-end iso-date="2018-12-31" />
  <value currency="EUR" value-date="2018-01-01">10000</value>
</budget>

.. code-block:: xml

<budget type="2" status="2">
  <period-start iso-date="2018-01-01" />
  <period-end iso-date="2018-12-31" />
  <value currency="EUR" value-date="2018-06-01">8000</value>
</budget>

**...**

.. code-block:: xml

<transaction>
  <transaction-type code="2" />
  <transaction-date iso-date="2018-01-01" />
  <value currency="USD" value-date="2018-01-01">10000</value>
</transaction>

.. code-block:: xml

<transaction>
  <transaction-type code="2" />
  <transaction-date iso-date="2018-06-01" />
  <value currency="USD" value-date="2018-06-01">-2000</value>
</transaction>

Activity Budgets should include:
--------------------------------

Please note:

-  Budgets are the amount of finance expected to be spent as part of an activity.

- Every activity that has planned or actual spend should have a budget.

- It is expected that the budget is described from the perspective of the reporting organisation.

- If for legal, commercial or humanitarian reasons a budget cannot be provided, the @budget-not-provided attribute should be used.

- Only one original and one revised budget should be published for each time period.

- Budgets can be updated at any point.

- The sum of all revised budgets, or original budgets if no revised budgets are present, should provide the current total budget for an activity.

- Budgets must be published in periods of no longer than a year. Publishing quarterly budgets is helpful for data users.

- An activity’s budget periods should not overlap.

- Budget values should not be negative.

- The sum of outgoing, or incoming, commitment transactions does not have to equal the total budget for an activity. These can differ depending on the publisher’s business model and legal framework.

-  The budget `status <http://reference.iatistandard.org/codelists/BudgetStatus/>`__ explains whether the budget being published is indicative or has been formally committed.

-  If no status is present, the budget is assumed to be indicative.

-  The `type <http://reference.iatistandard.org/codelists/BudgetType/>`__ describes if the budget is original or revised.

-  If no type is present, the budget is assumed to be original.

Technical guidance summary
--------------------------

**Activity Budget Information**

All activities should include the elements below, when publishing an activity budget.


+----------------+----------------+----------------+----------------+
| Element        | Use            | Rules          | Guidance       |
+----------------+----------------+----------------+----------------+
| `budget        | This provides  |                | The attributes |
| <http://refere | the financial  |                | type (original |
| nce.iatistanda | budget for the |                | or revised)    |
| rd.org/activit | activity,      |                | and status     |
| y-standard/iat | broken down by |                | (indicative or |
| i-activities/i | time periods   |                | committed)     |
| ati-activity/b | of a year or   |                | should be      |
| udget/>`__     | less.          |                | declared.      |
|                |                |                |                |
|                |                |                | If not         |
|                |                |                | declared, the  |
|                |                |                | budget is      |
|                |                |                | presumed to be |
|                |                |                | original and   |
|                |                |                | indicative.    |
+----------------+----------------+----------------+----------------+
| `period-s      | An iso-code    | The elements   | Publishing     |
| tart <http://r | for the start  | period-start   | budgets for    |
| eference.iatis | date of the    | and period-end | each quarter   |
| tandard.org/ac | budget.        | must appear    | is helpful for |
| tivity-standar |                | only once      | data users.    |
| d/iati-activit |                | within each    |                |
| ies/iati-activ |                | budget         |                |
| ity/budget/per |                | element.       |                |
| iod-start/>`__ |                |                |                |
+----------------+----------------+ The            |                |
| `period-end    | An iso-code    | period-start   |                |
| <http://refere | for the end    | date must be   |                |
| ne.iatistandar | date of the    | before or the  |                |
| d.org/activity | budget.        | same as the    |                |
| -standard/iati |                | period-end     |                |
| -activities/ia |                | date.          |                |
| ti-activity/bu |                |                |                |
| dget/period-en |                | The period     |                |
| d/>`__         |                | reported must  |                |
|                |                | be no longer   |                |
|                |                | than one year  |                |
+----------------+----------------+----------------+----------------+
| `value <h      | The financial  | This element   | The currency   |
| ttp://referenc | value of the   | must appear    | attribute is   |
| e.iatistandard | budget for the | only once      | required,      |
| .org/activity- | declared       | within each    | unless a       |
| standard/iati- | period.        | budget         | default        |
| activities/iat |                | element.       | currency has   |
| i-activity/bud | The            |                | been provided  |
| get/value/>`__ | `currency <h   | The value-date | for the        |
|                | ttp://referenc | must be        | activity.      |
|                | e.iatistandard | declared for   |                |
|                | .org/codelists | the value.     |                |
|                | /Currency/>`__ |                |                |
|                | and value-date |                |                |
|                | can also be    |                |                |
|                | declared for   |                |                |
|                | the value.     |                |                |
+----------------+----------------+----------------+----------------+
