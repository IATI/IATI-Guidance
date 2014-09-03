1.05 Changes
============

Changes / Additions to IATI Standard for version 1.05

Schema Changes
--------------

A full diff of all schema changes in 1.05 can be found in github at https://github.com/IATI/IATI-Schemas/compare/version-1.04...version-1.05#files_bucket

.. _1_05_activities_schema_changes:

Activities schema
~~~~~~~~~~~~~~~~~

:doc:`planned-disbursement </activity-standard/iati-activities/iati-activity/planned-disbursement>` 
(`discussion <http://support.iatistandard.org/entries/50424779-Add-a-description-in-the-schema-to-planned-disbursement-element>`__)

*Updated description text*

In 1.04:

======================  ========================
Element     	    	Description
======================  ========================
planned-disbursement	(none)
======================  ========================

Description added in 1.05:

======================  ========================
Element     	    	Description
======================  ========================
planned-disbursement	The planned disbursement element should only be used to report specific planned cash transfers. These should be reported for a specific date or a meaningfully predictable period. These transactions should be reported in addition to budgets - which are typically annual breakdowns of the total activity commitment.
======================  ========================


Organisations schema
~~~~~~~~~~~~~~~~~~~~
No substantial changes were made in 1.05, aside from essential version references.

Common schema
~~~~~~~~~~~~~~~~~~~~
No substantial changes were made in 1.05, aside from essential version references.

XML supplementary schema
~~~~~~~~~~~~~~~~~~~~~~~~~~
No substantial changes were made in 1.05, aside from essential version references.

Registry record schema
~~~~~~~~~~~~~~~~~~~~~~~
No substantial changes were made in 1.05, aside from essential version references.


Codelist Changes
----------------

New Codelists
~~~~~~~~~~~~~

No new codelists were added in 1.05


Updated Codelists
~~~~~~~~~~~~~~~~~

**Embedded codelist updates**:

:doc:`Activity Status </codelists/ActivityStatus>` 
(`discussion <http://support.iatistandard.org/entries/43247528-Activity-Status-Suspended->`__)

*New code*

===========  ===========  ========================
Code         Name    	  Description
===========  ===========  ========================
6	     Suspended	  a temporary suspension of an activity. In this state an activity is assumed not to be current, but future, forward-looking budgets are still assumed to be applicable.
===========  ===========  ========================

:doc:`Description Type </codelists/DescriptionType>` 
(`discussion <http://support.iatistandard.org/entries/22922878-Description-type-extend-the-codelist>`__)

*New code*

===========  ===========  ========================
Code         Name    	  Description
===========  ===========  ========================
4	     Other	  For miscellaneous use. A further classification or breakdown may be included in the narrative.
===========  ===========  ========================

:doc:`Document Type </codelists/DocumentType>` 
(`discussion <http://support.iatistandard.org/entries/86661313-Document-Types->`__)

*New codes*

===========  ============================================  ========================
Code         Name    	   				   Description
===========  ============================================  ========================
B11	     Sector strategy	      				       
B12	     Thematic strategy
B13	     Country-level Memorandum of Understanding
B14	     Evaluations policy
B15	     General Terms and Conditions
===========  ============================================  ========================

:doc:`Related Activity Type </codelists/RelatedActivityType>` 
(`discussion <http://support.iatistandard.org/entries/54201556-related-activity-new-code>`__)

*New code*

===========  ===========  ========================
Code         Name     	  Description
===========  ===========  ========================
5	     Third Party  A report by another organisation on the same activity (excluding activities reported as part of financial transactions - eg. provider-activity-id - or a co-funded activity using code = 4)
===========  ===========  ========================

*Amended code*

In 1.04:

===========  ===========  ========================
Code         Name    	  Description
===========  ===========  ========================
4	     Multifunded  A multifunded, or co-funded activity. The identifier should be globally unique and shared by all reporters of this activity.
===========  ===========  ========================

Name and description changed in 1.05:

===========  ===========  ========================
Code         Name     	  Description
===========  ===========  ========================
5	     Co-funded    An activity that receives funding from more than one organisation.
===========  ===========  ========================

:doc:`Transaction Type </codelists/TransactionType>` 
(`discussion <http://support.iatistandard.org/entries/50777388-Description-For-Transcation-Type-Incoming-Funds-Is-Incorrect>`__)

*Amended code*

In 1.04:

===========  ==============  ========================
Code         Name    	     Description
===========  ==============  ========================
IF	     Incoming Funds  Funds received from an external funding source (eg a donor).
===========  ==============  ========================

Description changed in 1.05:

===========  ==============  ========================
Code         Name     	     Description
===========  ==============  ========================
IF	     Co-funded       Funds received (whether from an external source or through internal accounting) for specific use on this activity.
===========  ==============  ========================


:doc:`Vocabulary </codelists/Vocabulary>` 
(`discussion <http://support.iatistandard.org/entries/22916773>`__)

*New code*

===========  =================================  ========================
Code         Name     	  			Description
===========  =================================  ========================
RO2	     Reporting Organisation (2)  	Where reporting organisations have more than one vocabulary that they wish to reference.
===========  =================================  ========================

:doc:`Policy Marker </codelists/PolicyMarker>` (`discussion <http://support.iatistandard.org/entries/52320903-New-Policy-Markers-Significance-Codes>`__)

*New code*

===========  ==================================================================  ========================
Code         Name     	  							 Description
===========  ==================================================================  ========================
9	     Reproductive, Maternal, Newborn and Child Health (RMNCH)
===========  ==================================================================  ========================


**Non-embedded codelist updates**:

:doc:`Policy Significance </codelists/PolicySignificance>` (`discussion <http://support.iatistandard.org/entries/52320903-New-Policy-Markers-Significance-Codes>`__)

*New code*

===========  =================================  ========================
Code         Name     	  			Description
===========  =================================  ========================
4	     Explicit primary objective
===========  =================================  ========================



Documentation Changes
---------------------

- Guidance added to :doc:`/overview/dates/`

    ActivityStatus code 6 indicates a temporary suspension of an activity. In this state an activity is assumed not to be current, but future, forward-looking budgets are still assumed to be applicable.

- Guidance updated for :doc:`/overview/classifications/` around used of ``TiedStatus`` codelist
(`commit <https://github.com/IATI/IATI-Extra-Documentation/commit/af04ae4cff33e1ee28cfe75c710bafdb61caf07b>`__)

- Guidance included for :doc:`Policy Significance </codelists/PolicySignificance>` codelist
