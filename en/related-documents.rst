Related documents
=================

Further information about an organisation or activity can be provided by using the **document-link** element. This link can be added to several places, including the organisation file. It can be attached to each activity, and at multiple points within a result element.

A publisher may want to add more detail about their work, such as the organisation’s annual report, the `conditions <http://reference.iatistandard.org/activity-standard/overview/conditions/>`__ *(new guidance coming soon)* attached to any funding, or a report on the results or impact the activity.

Where can related documents can be added?
-----------------------------------------


Please note:

-  Each document-link needs to contain a URL to a publicly accessible webpage or document.

-  The URL must begin with either ‘http://’ or ‘https://’.

-  If documents are available in other languages and stored separately, these should be added as additional document-link elements.

-  Including the `file-format <http://reference.iatistandard.org/codelists/FileFormat/>`__ attribute helps to inform users about what to expect from the document.

-  A number of donors require their grantees to publish specific documents.

Technical guidance summary
--------------------------

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1


   * - Location
     - Use
     - Rules
     - Guidance

   * - `organisation file <http://iatistandard.org/organisation-standard/iati-organisations/iati-organisation/document-link/>`__
     - Provides further information about the organisation or its work (e.g. their annual report or a work plan for a particular country).
     - There must be a URL for the external document or webpage.

       The document-link must include a title, format, and category.
     - A recipient country that is the focus of the document or webpage can be specified.

       A description of the document can also be added.

   * - `activity file <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/>`__
     - Links to further information about the activity.
     - There must be a URL for the external document or webpage.

       The document-link must include a title, format, and category.
     - The description should specify what the document is about and why it has been included.


**The locations below were introduced at version 2.03 of the IATI Standard:**

.. list-table::
   :widths: 14 43 43
   :header-rows: 1

   * - Location
     - Use
     - Guidance

   * - `result <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/document-link/>`__
     - A link to an online, publicly accessible webpage or document expanding on the result.
     - The document or webpage should link to the specific result being reported, or to a results frame.

   * - `indicator <http://iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/>`__
     - A link to an online, publicly accessible webpage or document expanding on the result indicator.
     - The document or webpage should link to the specific results indicator being reported.

   * - `baseline <http://iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/>`__
     - A link to an online, publicly accessible webpage or document expanding on the indicator’s baseline.
     - The document or webpage should link to the specific indicator baseline being reported.

   * - `period-target <http://iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/target/>`__ and `period-actual <http://iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/>`__
     - A link to an online, publicly accessible webpage or document expanding on period-target or period-actual.
     - The document or webpage should link to the specific target or actual figures being reported.


What a document-link should include

.. list-table::
   :widths: 14 43 43
   :header-rows: 1


   * - Element
     - Use
     - Rules

   * - `title <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/title/>`__
     - Short title of the document or webpage.
     - This must be included at once and only once for each document-link.

       The title can be provided in multiple languages.

   * - `description <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/description/>`__
     - Description of the document, including any instructions on where to find relevant information.
     - This element must occur no more than once for each document-link.

       The description can be provided in multiple languages.

   * - `category <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/category/>`__
     - Specifies the type of document or webpage.
     - This must be included once and only once for each document-link.

       The code must be on the `document category <http://iatistandard.org/codelists/DocumentCategory/>`__ codelist.

   * - `language <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/language/>`__
     - Specifies the language of the document or webpage.
     - The code must be on the `language <http://iatistandard.org/codelists/Language/>`__ codelist.

       If the document is available in multiple languages, the document-link element can be repeated with a different language code selected.

   * - `document-date <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/document-date/>`__
     - The date of publication or last updating
     - Must be in the format: YYYY-MM-DD, e.g. 2018-03-16.

.. meta::
  :title: Related documents
  :description: Further information about an organisation or activity can be provided by using the **document-link** element.
  :guidance_type: activity, organisation
  :date: September 19, 2019
