Publish your datafiles
^^^^^^^^^^^^^^^^^^^^^^

To publish your files you need to carry out the following: 




Validate Your IATI Files Using The IATI Validator
=================================================

The IATI Validator tool at http://validator.iatistandard.org/ will currently check your files for two things:

- That it contains only valid XML
- That it only uses elements as defined in the relevant version of the IATI Standard.

As a result, using the Validator is a two stage process. When you first upload or specify the URL of you file it carries out the check that the file only contains valid data. If no errors are found click on the 'Test Validation' link to make sure that the file contents conform to the IATI Standard.

If errors are found you should investigate and amend your original input CSV file data and recreate your files before re-validating to make sure that any problems have been fixed.




Move Your IATI Files to Your Own Web Servers 
============================================

IATI files should ideally be hosted on a publisher's own web servers. Once the files for publishing have been validated and contain no errors they should be moved to a location on the publisher's own web servers that has been previously identified to host them. 

it is important to consider that the URLs that are used to publish are:

- authoritative - eg: they are associated with a domain that you own (most preferably using publisher_name.org). Thus the published data has greater integrity and is generally considered 'credible' 
- stable - they are no subject to constant of frequent change. ``publisher_name.org/country1.xml`` would always be the URL for that country (not ``countryB.xml`` the next week!) 
- accessible - the URLs are not behind any security measures or any other means that would hinder access. (Note that access can also be hindered accidentally, due to a variety of technical reasons, see the :doc:`Accessing Data page of the Developer Documentation </developer/access/>` for more information).

It does not matter if the URLs are for a subdomain (data.{publisher}.org) or directory ({publisher}.org/data).

When publishing your IATI XML files it helps users if your server can be configured to:

- Provide a HTTP Content-type header indicating that the file is application/xml
- Provide a HTTP last-modified header indicating the last time that the file was modified

The last-modified header will help applications checking that they have the most up-to-date data to avoid fetching data that hasn't changed since they last looked, and so will reduce bandwidth and load on your servers. 

If you have created and published your files via Aidstream then you will need to login to your Aidstream account, click on 'List Published Files' and then for each file right click on the filename and select 'Save Link As ...' to download the file.

If you have created and published your files via the CSV Converter then you will need to login to your CSV Converter account and click on the model was used to generate your published files. Click on 'Convert' and then click on 'View Conversion History'. Put you cursor over the file that you want to download, right click on the filename and select 'Save Link As ...' to download the file.


 
Create An IATI Registry Account
===============================

All IATI publishers must have an account on the IATI Registry at http://www.iatiregistry.org/. The Registry is an index of data files published in compliance with the standards of the International Aid Transparency Initiative (IATI). It does not contain the actual data, only links to the published data, and metadata describing the contents of these files. When a publisher is close to publishing for the first time they should create an account on the IATI Registry. Once the account has been 'approved' by the IATI Secretariat the publishing organisation can add details of the location of their IATI XML datafiles. Once this has been done the publisher can consider themselves as having successfully published.


There are four steps involved in creating an account:

1. Register as a user
2. Create a New Publisher Account
3. Wait for your Publisher Account to be authorised by the IATI Secretariat
4. Register your datafiles


1. Register as a user
>>>>>>>>>>>>>>>>>>>>>

Submit your details at http://iatiregistry.org/user/register.


2. Create a New Publisher Account
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

Make sure that you are still logged into the user account created in 1. and navigate to “Create a New Publisher” on the “Publishers” menu. (This item will not display if you are not logged in.) 

Please fill in all the fields on the form following the advice associated with each field. There is a lot of data to provide but much of it can be found in your Implementation Schedule if you have created one.

Guidance on how to form your IATI Org ID can be found here: :doc:`iati-organisation-identifiers`


3. Wait for the Publisher Account To Be Authorised
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

This ensures that no-one can use the Registry to publish data purporting to come from an organisation that they are not authorised to represent. You will receive an email notifying you when the account has been authorised.


4. Add Details Of Your Datafiles
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

Once your publisher account has been authorised, log into it and select the 'Add Datafile' option in order to add the details and URL location of your IATI datafiles that you are publishing. 



5. Bulk Upload Details Of Your Datafiles
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

If a Publisher has a large number of datafiles to add to the Registry they can do a bulk upload using a CSV file rather than adding each one manually and individually .

The CSV file template and guidance for how to do this can be found at: http://www.iatiregistry.org/csv/upload or by hovering over ‘Data’ and clicking on ‘upload CSV file’.

Most of the fields are self-explanatory and relate to the ‘Add a Datafile’ form that would be completed if adding files manually. The template requires each file to be a line in the CSV file. For each line (file) the ‘registry-publisher-id’ which is the publisher ID used to set up the publisher account on the Publisher's Registry account is required. A ‘registry-file-id’ is also needed. This identifies the data covered in the file through including country or region coding or the file type (activity or org). Further information on this can be found in the section above on uploading individual files.

Once the CSV file has been completed and saved it can be uploaded to add the Datafile details files by clicking on ‘Choose file’, selecting the CSV file and then clicking on ‘upload’ .
