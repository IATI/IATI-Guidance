Updating Your Data and Organisation Details
^^^^^^^^^^^^^^^^^^

Once you have initially published your first data sets you need to ensure that they are updated regularly. The IATI Technical Team recommends that as a minimum each organisation should be updating their data quarterly. 

The IATI Standard recognises that organisation details do change over time. The sections below cover the key changes that publishers might need to make.



Regularly Updating Your Datafiles
=================================

Once an organisation has committed to publish to IATI, it is most important that their data files are updated regularly and in line with the frequency as specified in a publisher's IATI Registry account. 

When updating your data, the additions should be added to existing activities. Publishers should NOT create additional new files that only contain the most recent information. Ideally all the information that relates to a specific activity should be kept together as this makes the use and analysis of the data third parties much more efficient. Data should be cumulative (e.g. if publishing every quarter, the new files will include the quarter being reported on, and the previous quarter reported last time, and so on). It will also enable amendments to be made to existing data.

No data should ever be removed or deleted from published files. It is intended that once published, data remains permanently available. However, it is recognised that at certain points data will need to be moved or merged into other activities. If two activities are merging, organisations need to ensure that all the information is transferred across and nothing is lost.

If an activity ID needs to change this should be recorded within the activity by the use of the element `<other-identifier> <http://iatistandard.org/202/activity-standard/iati-activities/iati-activity/other-identifier/>`__.

You will need to refer to the specific guidance of the tool that you are using to publish in order to find out how to update pre-existing datasets.




Change of Organisation IATI Contact
===================================

As people frequently change job it is quite common that the nominated point of contact for IATI within an organisation will change over time. When this occurs please contact the IATI Technical Support Team by emailing us at support@iatistandard.org to let us know the name of the new contact so that we can update our records accordingly.

In addition, the name of the IATI point of contact should be updated in the IATI Registry (check your user account, publisher account and datafiles for contacts details).




Change of Organisation Name
=========================

If an organisation has legally changed their name this can be updated on the IATI Registry. This can be done by going to their publisher page and clicking the 'manage' button on the top right hand side. The name should also be updated in an organisation's IATI organisation and activity files. The publisher's name is likely to be included in the `<reporting-org> <http://iatistandard.org/202/activity-standard/iati-activities/iati-activity/reporting-org/>`__, `<participating-org> <http://iatistandard.org/202/activity-standard/iati-activities/iati-activity/participating-org/>`__ and `<narrative> <http://iatistandard.org/202/activity-standard/iati-activities/iati-activity/participating-org/narrative/>`__ elements.

Two further points should be considered:

1) The publisher should decide if they want to change their Registry Publisher ID to something that more closely matches their new name. If this is the case, the steps under 'Changing an Organisation's Publisher ID' should be followed.

2) If the change of name is due to a structural or legal change, and has essentially become a new organisation, e.g. it has merged with another organisation and/or has re-registered with its regulating body then its IATI Org ID will need to be changed. If this is the case, the steps under 'Changing an Organisation’s IATI Org ID' should be followed. 


Changing an Organisation's IATI Org ID
========================

Each publisher account on the IATI Registry needs to be approved by the IATI Technical Team. This ensures that organisations are using the correct IATI Org ID. Once an account has been approved the organisation's IATI Org ID should not be changed unless there is a structural or legal change which requires this e.g. the organisation has essentially become a new organisation by merging with another organisation and/or has re-registered with its regulating body.

A number of steps need to be followed to ensure that data users can continue to use the organisation's data efficiently:

1) The publisher should alert the IATI Technical Team via: support@iatistandard.org, that they are planning on updating their IATI Org ID and what it will be and what action they are intending to take regarding their published IATI files.

2) On the IATI Registry the publisher needs to update their IATI Org ID. This is done by logging in to the IATI Registry and going to the organisation's Publisher Page. There is a 'manage' button on the top right side of the page, and will allow the information about the organisation to be updated.

3) The publisher should update any of their new or existing published IATI files. In every occasion where the organisation's IATI Org ID is mentioned e.g. in the `<reporting-org> <http://iatistandard.org/202/activity-standard/iati-activities/iati-activity/reporting-org/>`__ element this should be updated. As Activity ID's also use the organisation's IATI Org ID these need to be updated too.

4) When all the Activity IDs are updated the element `<other-identifier> <http://iatistandard.org/202/activity-standard/iati-activities/iati-activity/other-identifier/>`__ should be added with the attributes @ref and @type. The @ref attribute should contain the previous Activity ID and the  `@type <http://iatistandard.org/202/codelists/OtherIdentifierType/>`__ code should be 'A3', which is 'Previous Activity Identifier'.



Changing an Organisation's Publisher ID
=======================

Each publisher account on the IATI Registry has a unique Publisher ID. This is usually an abbreviation of the publisher's name and is used as part of the URL for their publisher page on the internet. An organisation can change their publisher ID at any point but they need to follow the steps below to ensure that tools which use IATI data can still import the organisation's published IATI xml files correctly.

The steps to follow are:

1) The publisher should contact the IATI Technical Support Team to let them know that the organisation is planning its Publisher ID.

2) The publisher should update the Registry Publisher ID. This can be done by logging into the IATI Registry, going to the publisher page and clicking on 'manage' on the top side of the page. If using a publishing tool, the organisation should check if they need to update their publisher ID on this tool too e.g. this is the case when using Aidstream.

3) The publisher should delete all existing datafiles from their publisher account. This removes the connection between the IATI Registry and their IATI xml files but does not delete the place where the actual files are hosted. This can be done by clicking on the 'Datasets' tab once the Publisher ID has been updated.

4) The publisher should then re-publish their datafiles to their updated Registry Publisher Account.

5) The IATI Technical Support Team will then arrange for redirects from the old datasets to be set up so that any third party users of the organisation's datafiles will be able to find the new files.
