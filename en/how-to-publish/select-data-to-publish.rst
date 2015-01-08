Data considerations
^^^^^^^^^^^^^^^^^^^^^


Deciding what data to publish can be aided by filling out the Organisation and Activity tabs of the Implementation Schedule.


The Role Of the IATI Standard
=============================

The IATI Standard is fundamental to the publishing process because the it provides the specification for how data must be formatted for IATI publishing. 

The IATI Standard has three main components:

 * :doc:`/organisation-standard`- which provides the definition for what data can be included and how it must be formatted for the Organisation file
 * :doc:`/activity-standard/` - which provides the definition for what data can be included and how it must be formatted for an Activity file
 * :doc:`/codelists/` - provide the definitive list of allowed values for specific data elements or attributes

The IATI Standard is managed by the IATI Secretariat and anyone can request amendments or changes to the IATI Standard via the IATI Standard Upgrade process - see http://iatistandard.org/upgrades .



Deciding What Data To Publish
=============================

When working towards publication, it is important to know what data you have available as an organisation and the quality of this data. The focus is very much on publishing what you can, based on what is readily available, ensuring it is of reasonable quality, and also taking into account any exclusions. The idea is to then continually improve over time.

Publishers should try and consider publishing data for all fields of the IATI Standard. However, it is recognised that some elements will not be relevant to all organisations or information in some areas may need to be excluded for reasons of security or confidentiality.

IATI recognises that an organisation is unlikely to have all of the information set out in the IATI Standard available for immediate publication. An organisation can therefore work with whatever information they currently have available with the aim of adding to this as they progress through the IATI process. 

The 'Organisation' and Activity' tabs of the Implementation Schedule allows organisations to identify what information is available for immediate publication, what is only partially publishable (e.g. may require further information to be added in before reaching full implementation), and what will be published at a future date. It also enables organisation to state what data is not available, whether this is due to exclusions or it not being applicable to the organisation for example, and what is not currently captured but could be considered for publication at some stage.
 
The availability of data will also depend on how information is currently captured and stored – i.e. does it need to be drawn from different places to meet IATI requirements? Delays in publishing beyond what is immediately available could therefore be due to having to put new systems in place to integrate data capture mechanisms.




Segmenting Files & File Size
=============================

It is recommended that publishers segment their files to ensure that no file is larger than 40MB in size. Whilst there is no definitive rule as to when a file is too large, we recommend a maximum file size in order to minimise any issues of file processing by both IATI and third parties data users.

With regard to segmentation, there is no definitive best practice for how files should be segmented. By country was historically the preferred option but this is no longer a requirement because published data can now be queried more easily via the IATI Datastore. The publisher should therefore carry out segmenetation on whatever makes most sense to their publishing process. Examples might be by country, by region, by grant or loan type etc. As data volumes have increased some publisher are now segmenting by open and closed activities. This has the benefit that once created, there is no further requirement to reproduce or update a file of closed projects each time the Publisher updates their data. 




Character Encoding
==================

The use of the Unicode UTF-8 or UTF-16 character encodings is strongly recommended to provide support for the widest range of languages.  These encodings may be declared at the beginning of XML documents as follows:

.. code-block:: xml
   
   <?xml version="1.0" encoding="UTF-8"?>

or

.. code-block:: xml

   <?xml version="1.0" encoding="UTF-16"?>

The XML standard requires all conforming software to support both of these encodings, so the choice is up to the publisher.  In most cases, UTF-8 should result in smaller documents even for non-alphabetic languages like Han Chinese, since much of an IATI document consists of XML markup, (alphabetic) codes, and numeric values.

it is recommended that  non-Unicode character encodings such as “BIG5” or “ISO-8859-1” are NOT used, since these might not be supported by all XML processing software, and the Initiative’s goal is maximum transparency and portability.




DFID Minimum Requirements (UK NGOs and their Partners)
======================================================

If you are a DFID grantee then you need to make sure that you include all the fields that have been designated as mandatory by DFID. The list of these fields is at https://drive.google.com/file/d/0B32cSl_hOcDjalJqWWlCeDRVMW8/edit?usp=sharing

