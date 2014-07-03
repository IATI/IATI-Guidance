Frequently Asked Questions
^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. contents ::

 
Who Can Publish To IATI?
=========================

Anybody who is providing 'aid' can publish data using the IATI standards. The different types of 'aid' are described at http://iatistandard.org/codelists/AidType/ 

- small NGOs
- national civil society organisations
- international aid agencies
- donors or foundations
- governments
- multilateral institutions
- private sector organisations




What Is A 'Schema'
===================

For IATI, the phrase "schema" refers to an XML Schema Definition (XSD), which is standard XML-related technology. An XSD is usually a file (commonly with an .xsd extension) that describes the expected content of an XML document. The XSD file can be used to check whether a particular XML document is "valid", i.e. it conforms to its expected content.

For example, at first glance the following IATI activities XML appears valid:

.. code-block:: xml

    <iati-activities>
      <iati-activity language="en">
        <reporting-organisation ref="GB-1" />
        <iati-identifier>GB-1-999999-999</iati-identifier>
        <title>Activity Title</title>
      </iati-activity>
    </iati-activities>

However, the iati-activities-schema.xsd file contains the details of all the valid attributes and elements, as described in the IATI standard. If the XSD was used to validate the example XML then it would reveal that the XML contains the invalid element ``<reporting-organisation>``, instead of the correct element ``<reporting-org>``.

Interestingly, XSDs are actually XML documents. So we are using XML to validate XML!




What Is XML?
============

XML stands for eXtensible Markup Language. It is a standard way of representing data that can be interpreted by computers and quite easily read by humans! It differs from many other formats in that it describes both data and the structure of that data. For example:

.. code-block:: xml

    <name>
      <title>Mr</title>
      <forename>James</forename>
      <surname>Clark</surname>
    </name>

This example depicts a structure where a name is comprised of a title, a forename and a surname, and also shows the data for Mr James Clark (who was responsible for the term "XML").


 
 
Do I Need To Understand XML. It Looks A Bit Scary?
==================================================

It depends. If you are not involved in the physical production of IATI data then no. If you are, then possibly.

However, there isn't really very much to XML, so a brief example should demystify it and explain the associated terminology:

.. code-block:: xml

    <cars>
      <car>
        <manufacturer>Ford</manufacturer>
        <model>Focus</model>
        <price currency="GBP">10000</price>
        <specification>
          <equipment type="Standard">CD Player</equipment>
          <equipment type="Optional">Heated Seats</equipment>
        </specification>
      </car>
      <car>
        <manufacturer>Honda</manufacturer>
        <model>Civic</model>
        <price currency="GBP">5000</price>
        <specification />
      </car>
    </cars>

This example shows the 3 main concepts of XML: elements, attributes and content.

Elements represent the main building blocks of an XML document. They are represented using "tags", which are denoted using the characters ``<`` and ``>``. In the example, ``<cars>`` is the opening tag of the cars element and ``</cars>`` is the closing tag, distinguished by the forward-slash character (/). Elements can contain other elements or just text, or they can be empty. Empty elements can either be represented by placing their opening and closing tags together (e.g. ``<specification></specification>``) or, as shown in the example, by using the empty-element tag (e.g. ``<specification />``), which combines the opening and closing tags into a single tag. In the example cars, car, manufacturer, model, price and specification are all elements.

Attributes provide additional information about an element and are listed within an opening tag or empty-element tag. They have both a name and a value and the value is always enclosed in quote marks (``"``). In the example, currency and type are attributes.

Content is text that appears between elements' opening and closing tags that does not represent other elements. In the example, the text "Ford", "Honda", "Focus", "Civic", "10000", "5000", etc. are examples of content.

For more detailed information about XML, see http://en.wikipedia.org/wiki/XML or http://www.w3schools.com/xml/default.asp.
