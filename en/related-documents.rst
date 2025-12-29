Related documents
=================

Further information about an organisation or activity can be provided using the *document-link* element. This link can be added in the organisation file, or attached to individual activities.

A reporting organisation may want to add more detail about their work, such as the organisation’s annual report, the `conditions <http://reference.iatistandard.org/activity-standard/overview/conditions/>`__ attached to funding, or the evaluation of an activity.


How do I add document links?
-----------------------------

-  Each *document-link* needs to contain a URL to a publicly accessible webpage or document.

-  If documents are available in other languages and stored separately, these should be added as separate *document-link* elements.

-  Including the document `format <http://reference.iatistandard.org/codelists/FileFormat/>`__ attribute informs users about what to expect from the document.

-  A number of donors require their grantees to publish specific documents.


Recommendations
-----------------
We suggest three simple actions to significantly improve document link usability:

**1. Link directly to documents, not document pages**

Almost 30% of links point to HTML pages. These are sometimes valid (project web pages, for example) but they are often web pages that contain links to the actual documents. This extra step hinders automated software access, even if it's acceptable for human users.

**2. Update your links to https where applicable**

Many historic links use http instead of https (e.g., http://example.org instead of https://example.org). Most sites have upgraded to https now, so the links need updating.

**3. Ensure your links are available**

Check the percentage of inaccessible documents using the Availability tab on the Organisation Detail page. Focus on:

- 403: Access denied. Consult your web team.
- 404: Broken or missing link. Check the address (URL).



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
     - Provides further information about the organisation or its work - e.g. their annual report or a work plan for a particular country.
     - There must be a URL for the external document or webpage.

       The document-link must include a title, format, and category.
     - A recipient country that is the focus of the document or webpage can be specified.

       A description of the document can also be added.

   * - `activity file <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/>`__
     - Links to further information about the activity.
     - There must be a URL for the external document or webpage.

       The document-link must include a title, format, and category.
     - The description should specify what the document is about and why it has been included.


**What a document-link should include:**

.. list-table::
   :widths: 14 43 43
   :header-rows: 1

   * - Element
     - Use
     - Rules

   * - `title <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/title/>`__
     - Short title of the document or webpage.
     - This must be included once and only once for each *document-link*.

       The title can be provided in multiple languages.

   * - `description <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/description/>`__
     - Description of the document, including any instructions on where to find relevant information.
     - This element must occur no more than once for each *document-link*.

       The description can be provided in multiple languages.

   * - `category <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/category/>`__
     - Specifies the type of document or webpage.
     - At least one category must be published for each *document-link*.

       The code must be on the `document category <http://iatistandard.org/codelists/DocumentCategory/>`__ codelist.

   * - `language <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/language/>`__
     - Specifies the language of the document or webpage.
     - The code must be on the `language <http://iatistandard.org/codelists/Language/>`__ codelist.

       If the document is available in multiple languages, the *document-link* element can be repeated with a different language code selected.

   * - `document-date <http://iatistandard.org/activity-standard/iati-activities/iati-activity/document-link/document-date/>`__
     - The date of publication or last updating
     - Must be in the format: YYYY-MM-DD, e.g. 2018-03-16.


**The locations below were deprecated in [month, 2026], after being part of version 2.03 of the IATI Standard:**

- `result <http://reference.iatistandard.org/activity-standard/iati-activities/iati-activity/result/document-link/>`__
- `indicator <http://iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/>`__
- `baseline <http://iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/baseline/>`__
- `period-target <http://iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/target/>`__ and `period-actual <http://iatistandard.org/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/>`__


.. meta::
  :title: Related documents
  :description: Further information about an organisation or activity can be provided by using the **document-link** element.
  :guidance_type: activity, organisation
  :date: December 29, 2025
