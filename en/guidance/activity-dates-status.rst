Activity dates and status
=========================

Each activity published to IATI should specify the time period in which the activity took place. Both the planned start and end dates of an activity can be provided, then the actual start and end dates can be added when known. Each organisation can choose the point at which an activity has started and ended.

Within an activity, the transactions, budgets, planned-disbursements and indicators can be published. Each of these should contain a specific date or time period.

Activities can also be given a ‘status’, such as ‘closed’ or ‘cancelled’. These help data users understand what stage an activity is at. It’s important that the status of an activity is kept up to date.

What activity information can be published?
-------------------------------------------

Please note:

-  Dates must be in the format YYYY-MM-DD, e.g. 2018-03-16.

-  Dates can be updated at any point.

-  Activities can be published at any point: when they are planned, ongoing or completed.

-  There are two types of date: planned and actual.

   -  Planned start and planned end dates represent when the project was expected to start or end. These dates can be in the future.

   -  Actual start and actual end dates represent the actual start and end dates. These should be published in addition to the planned dates, only once the activity has actually started or ended. These dates must not be in the future.

Technical guidance summary
--------------------------

All activities must include the activity-date and activity-status elements.

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `activity-date <http://iatistandard.org/activity-standard/iati-activities/iati-activity/activity-date/>`__
     - Provides the period of time in which the activity happened, or  is planned to happen in.

       This element includes the date and a code declaring the `type <http://reference.iatistandard.org/codelists/ActivityDateType/>`__ of date.
     - Either a planned or actual start date must be provided.

       A planned start date must be before or equal to the planned end date.

       An actual start date must be before or equal to the actual end date.

       Actual start and end dates must not be in the future.
     - End dates should, wherever possible, reflect the ending of the activity.

       If the actual dates are not known, planned start and end dates should be provided.

       Once work on the activity has finished, an actual end date should be added.

   * - `activity-status <http://iatistandard.org/activity-standard/iati-activities/iati-activity/activity-status/>`__
     - Describes the current `status <http://iatistandard.org/codelists/ActivityStatus/>`__ of the activity (e.g. 4 = closed)
     - This element must appear only once for each activity.
     - The status of the activity should be updated at each stage, such as whenever an actual start or end date is added.
