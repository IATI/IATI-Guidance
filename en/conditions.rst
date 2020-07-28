Conditions
==========

IATI asks publishers to declare any conditions or specific terms that are attached to their activities. For example, these could be the requirements issued by a funder or a six month review to assess whether or not the activity is worth continuing.

IATI data should first flag whether or not there are conditions attached to an activity in the `conditions <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/conditions/>`__ element. A short description should be included which explains each of the attached conditions. If there are no conditions attached to the activity, it is strongly recommended that the element is used to declare ‘no conditions’.

More detail about an activity’s conditions can be added by using the :doc:`document-link <related-documents>` element. For example, this could include a link to the agreed terms of reference between the organisation carrying out the work and its funder. It is good practice to include in the short description of the condition that further information can be found in a document-link.

**Conditions should include:**

-  It is recommended that every activity contains a conditions element. It is valid to declare that no conditions are attached.

-  When multiple conditions exist, these can be reported separately within the conditions element.

-  The conditions can be repeated in multiple languages, using separate narrative elements.

-  Three types of condition can be reported:

   -  **Policy**: e.g. a particular policy needs to be implemented by the receiving organisation.

   -  **Performance**: e.g. certain outputs or outcomes need to be achieved

   -  **Fiduciary**: e.g. the recipient is required to use certain public financial management or public accountability measures.

-  Further details about a condition can be supplied using the activity :doc:`document-link <related-documents>` element.

-  If a condition relates to the whole organisation, such as organisation-wide terms and conditions, it should not be reported within an activity. Rather, it should be included as a document-link in the organisation file.

Technical guidance summary
--------------------------

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Element
     - Use
     - Rules
     - Guidance

   * - `conditions <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/conditions/>`__
     - Specifies if there are terms and conditions attached to an activity.
     - This element must occur no more than once for each activity.

       The element must contain one @attached boolean. This states whether or not conditions are attached to the activity.

     - When using the @attached boolean:

       1 = yes

       0 = no

   * - `condition <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/conditions/condition>`__
     - Contains details of a condition.
     - The type of condition must be provided using the `type <http://reference.iatistandard.org/codelists/ConditionType/>`__ attribute: policy, performance or fiduciary.
     - This element can be repeated multiple times

       The description of the condition is held within the narrative element.

       If a condition relates to a whole organisation, it should not be reported here. Rather, it should be included as a document link in the organisation file.

   * - `narrative <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/conditions/condition/narrative/>`__
     - Short description of the condition.
     -
     - Further details about a condition can be supplied using the activity :doc:`document-link <related-documents>` element.

.. meta::
  :title: Conditions
  :description: IATI asks publishers to declare any conditions or specific terms that are attached to their activities.
  :guidance_type: activity
  :date: July 27, 2020
