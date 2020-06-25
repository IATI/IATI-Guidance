Publishing data on COVID-19 using the IATI Standard
===================================================

Following a `consultation with IATI’s community <https://discuss.iatistandard.org/t/covid-19-iati-publishing-guidance-consultation/1925>`__, this guidance has been updated to provide **additional recommendations** on how to publish data on COVID-19 using the IATI Standard.

Who is this guidance for?
-------------------------

This document provides instructions on how organisations can publish data about their activities in response to the COVID-19 pandemic. It is written for organisations who are already registered as IATI publishers and have previously published IATI data files on their development and/or humanitarian work. The guidance may be updated as the COVID-19 pandemic evolves and as further feedback is received from the IATI community of publishers and members. International development and humanitarian actors not already registered to publish IATI data are encouraged to contact IATI’s `Technical Team <mailto:support\@iatistandard.org>`__ for support on getting set up to publish data on COVID-19 to IATI.

What data should I publish?
---------------------------

Organisations who are involved in the international effort to address the COVID-19 pandemic are strongly encouraged to publish data on **all their activities and spending**. This includes activities and/or transactions associated with managing a **humanitarian emergency**, for example, a UN agency launching an international appeal to fund their response or an NGO delivering increased medical and food supplies. This also includes **longer-term development activities**, for example, a donor providing additional funding for debt relief to developing countries affected by public health disasters. It might also include transactions in ongoing activities with the specific purpose of contributing to a humanitarian emergency.

How do I publish data on COVID-19?
----------------------------------

Organisations should publish data on their activities responding to COVID-19 using the specific reporting guidance below. IATI has already been in conversation with UN OCHA Financial Tracking Service, ensuring alignment with their reporting guidelines and the Global Humanitarian Response Plans, as well as with the World Health Organisation and the Humanitarian Data Exchange making sure we are aligned.

Using specific IATI Standard elements to provide COVID-19 data
--------------------------------------------------------------

**1. Title and Description** [1]_

Add “COVID-19” in the `title <http://reference.iatistandard.org/203/activity-standard/iati-activities/iati-activity/title/>`__ of reported activities. If organizations are unable to specify COVID-19 in the activity title, they can include “COVID-19” in the activity descriptions and/or transaction descriptions.

**2. Humanitarian Scope element**

In the `humanitarian scope element <http://reference.iatistandard.org/203/activity-standard/iati-activities/iati-activity/humanitarian-scope/>`__\ we strongly recommend using both the Emergency (1) and Appeal (2) `type codelists <http://reference.iatistandard.org/203/codelists/HumanitarianScopeType/>`__ and respective `vocabulary for GLIDE and Humanitarian Response Plan (HRP) codes <http://reference.iatistandard.org/203/codelists/HumanitarianScopeVocabulary/>`__ when reporting activities related to COVID-19. You should do that by specifying:
  
* GLIDE Appeal related to COVID-19- “EP-2020-000012-001” [2]_

.. code-block:: xml

  <humanitarian-scope type="1" vocabulary="1-2" code="EP-2020-000012-001"/>

* Humanitarian Response Plans related to COVID-19- “HCOVD20” [3]_

.. code-block:: xml

  <humanitarian-scope type="2" vocabulary="2-1" code="HCOVD20"/>

* *Note:* You are advised to use the humanitarian-scope element irrespective of whether the activity you are reporting classifies as development or humanitarian funding.

**3. Humanitarian flag**

Use the humanitarian attribute for humanitarian activities and/ or transactions related to COVID-19:

.. code-block:: xml

  <iati-activity humanitarian="1" >

.. code-block:: xml

  <transaction humanitarian="1">

* *Note:* Not all activities responding to the COVID-19 pandemic will be classified as ‘humanitarian’, so please only use the Humanitarian flag where relevant.

**4. Tag**  [4]_

If an organization does not permit the publishing of data in the Humanitarian Scope for their development activities, they can publish "COVID-19" within the `Tag data field <http://reference.iatistandard.org/203/activity-standard/iati-activities/iati-activity/tag/>`__. In order to do this, publishers use vocab= "99", treat it as free text, and add "COVID-19".

.. code-block:: xml

  <tag vocabulary="99" code="COVID-19">

Providing timely and comprehensive data
---------------------------------------

In addition to the use of IATI elements described above, it is also very important that your organisation publish timely and comprehensive data. Organisations should publish information as quickly as possible and update it regularly with progress on the implementation of the activity.

Please **do not** publish only the minimum required data, but make use of all the IATI elements to provide useful context about your work. For example, publish detailed titles and descriptions, specify the partners involved in the activities and refer to them by their IATI organisation identifier in combination with the IATI activity identifier where possible. Do also include geographic information, results data and all other fields that help to describe your work. Please see IATI’s `updated guidance <https://iatistandard.org/en/news/interpreting_iatis_standard_made_easier_with_new_guidance/>`__ for information on publishing data to specific IATI Standard elements.

How can I receive further support on publishing COVID-19 activities?
--------------------------------------------------------------------

If you have any specific questions on publishing activities related to COVID-19, please do get in touch with the IATI Secretariat by emailing the `IATI Helpdesk <mailto:support\@iatistandard.org>`__.

See archived copy of `Version 1 - 27 March 2020 Guidance: Publishing data on COVID-19 using the IATI Standard <https://drive.google.com/file/d/1maA508bwKnLvcHdDe6eSItEz-w2SiPoE/view?usp=sharing>`__

.. [1]
   This was added to Version 2 Guidance: Publishing data on COVID-19 using the IATI Standard

.. [2]
   The GLIDE code (EP-2020-000012-001) has now been added- see `here <https://data.humdata.org/dataset/unocha-glides>`__. It follows the format of GLIDE codes with the last three digits ‘001’, specifying that this is a global emergency.

.. [3]
   The Global Humanitarian Response Plan (HRP) (`HCOVD20 <https://fts.unocha.org/plan-code-list-iati>`__) is provided by UNOCHA Financial Tracking Service (FTS) and is in addition to all existing humanitarian response plans. There are currently no overlapping requirements between HRP `HCOVD20 <https://fts.unocha.org/plan-code-list-iati>`__ and existing HRPs on to COVID-19. For any updates, keep an eye on the `FTS site <https://fts.unocha.org/plan-code-list-iati>`__.

.. [4]
   This was added to Version 2 Guidance: Publishing data on COVID-19 using the IATI Standard

.. meta::
  :title: Guidance: publishing data on COVID-19 using the IATI Standard
  :description: Following a `consultation with IATI’s community this guidance has been updated to provide recommendations on how to publish data on COVID-19 using the IATI Standard.
  :guidance_type: activity
