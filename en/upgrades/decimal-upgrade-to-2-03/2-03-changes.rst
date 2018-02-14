2.03 Changelog
^^^^^^^^^^^^^^

Changes / additions to IATI Standard for version 2.03

Note: Version 2.03 was released on Monday 19th February 2018.

.. contents::


.. _2_03_schema_changes:

Schema Changes
==============

A full diff of all schema changes in 2.03 can be found in the `IATI GitHub <https://github.com/IATI/IATI-Schemas/compare/version-2.02...version-2.03#files_bucket>`__

Activities Schema
-----------------

- Added new @crs-channel-code attribute for the participating-org element (`#338 <https://github.com/IATI/IATI-Schemas/issues/338>`__) (`discussion link <https://discuss.iatistandard.org/t/crs-channels-of-delivery-included-2-03/857>`__)

- Added new tag element (as a child of the iati-activity element) (`#342 <https://github.com/IATI/IATI-Schemas/issues/324>`__) (`discussion link <https://discuss.iatistandard.org/t/non-statistical-secondary-sectors-excluded-2-03/849>`__)

- Updated definition: [recipient-country, recipient-region, sector] @percentage attribute (`#343 <https://github.com/IATI/IATI-Schemas/issues/343>`__) (`discussion link <https://discuss.iatistandard.org/t/boundary-values-for-percentages-included-2-03/843>`__)

- Updated definition: sector @vocabulary attribute (`#344 <https://github.com/IATI/IATI-Schemas/issues/344>`__). The % sign was removed.

- Updated definition: [transaction aid-type, default-aid-type] @code attribute (`#345 <https://github.com/IATI/IATI-Schemas/issues/345>`__) (`discussion link <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__)

- Added new @vocabulary attributes for elements relating to aid-type (`#346 <https://github.com/IATI/IATI-Schemas/issues/346>`__) (`discussion link <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__)

- Updated definition: capital-spend @percentage attribute (`#348 <https://github.com/IATI/IATI-Schemas/issues/348>`__) (`discussion link <https://discuss.iatistandard.org/t/boundary-values-for-percentages-included-2-03/843>`__)

- Updated definition: related-activity element (`#349 <https://github.com/IATI/IATI-Schemas/issues/349>`__) (`discussion link <https://discuss.iatistandard.org/t/hierarchies-related-activity-definition-included-2-03/840>`__)

- Updated occurrence: default-aid-type element (`#350 <https://github.com/IATI/IATI-Schemas/issues/350>`__) (`discussion link <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__)

- Updated occurrence: transaction aid-type element (`#351 <https://github.com/IATI/IATI-Schemas/issues/351>`__) (`discussion link <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__)

Changes and Additions to the **Result** element:

- Updated definition: result/indicator/reference @indicator-uri attribute (`#347 <https://github.com/IATI/IATI-Schemas/issues/347>`__) (`discussion link <https://discuss.iatistandard.org/t/guidance-on-u-r-i-usage-for-publisher-s-own-vocabularies-included-2-03/850>`__)

- Updated occurrence: result/indicator/baseline element  (`#352 <https://github.com/IATI/IATI-Schemas/issues/352>`__) (`discussion link <https://discuss.iatistandard.org/t/results-improve-consistency-of-results-standard-included-2-03/874>`__)

- Updated occurrence: result/indicator @value attributes (`#353 <https://github.com/IATI/IATI-Schemas/issues/353>`__) (`discussion link <https://discuss.iatistandard.org/t/results-represent-more-than-quantitative-data-included-2-03/872>`__)

- Updated occurrence: [result/indicator/period/target, result/indicator/period/target/actual] elements (`#354 <https://github.com/IATI/IATI-Schemas/issues/354>`__) (`discussion link <https://discuss.iatistandard.org/t/results-allow-disaggregations-of-results-data-included-2-03/871>`__)

- Updated occurrence: result/indicator/period/target @value attribute (`#355 <https://github.com/IATI/IATI-Schemas/issues/355>`__) (`discussion link <https://discuss.iatistandard.org/t/results-represent-more-than-quantitative-data-included-2-03/872>`__)

- Updated occurrence: result/indicator/period/actual element (`#356 <https://github.com/IATI/IATI-Schemas/issues/356>`__) (`discussion link <https://discuss.iatistandard.org/t/results-allow-disaggregations-of-results-data-included-2-03/871>`__)

- Updated occurrence: result/indicator/period/actual @value attribute (`#358 <https://github.com/IATI/IATI-Schemas/issues/358>`__) (`discussion link <https://discuss.iatistandard.org/t/results-represent-more-than-quantitative-data-included-2-03/872>`__)

- Added new document-link element (as a child of various result elements)(`#359 <https://github.com/IATI/IATI-Schemas/issues/359>`__) (`discussion link <https://discuss.iatistandard.org/t/add-document-link-to-results-indicator-included-2-03/895>`__)

- Added new reference element (as a child of the result element) (`#362 <https://github.com/IATI/IATI-Schemas/issues/362>`__) (`discussion link <https://discuss.iatistandard.org/t/results-vocabulary-attribute-option-included-2-03/879>`__)

- Added new @aggregation-status attribute for the indicator element (`#363 <https://github.com/IATI/IATI-Schemas/issues/363>`__) (`discussion link <https://discuss.iatistandard.org/t/results-improve-consistency-of-results-standard-included-2-03/874>`__)

- Added new location element (as a child of the baseline element) (`#365 <https://github.com/IATI/IATI-Schemas/issues/365>`__) (`discussion link <https://discuss.iatistandard.org/t/results-improve-consistency-of-results-standard-included-2-03/874>`__)

- Added new dimension element (as a child of the baseline element) (`#366 <https://github.com/IATI/IATI-Schemas/issues/366>`__) (`discussion link <https://discuss.iatistandard.org/t/results-allow-disaggregations-of-results-data-included-2-03/871>`__)

Organisations Schema
-------------------

- Updated definition: organisation-identifier element (`#361 <https://github.com/IATI/IATI-Schemas/issues/361>`__) (`discussion link <https://discuss.iatistandard.org/t/migration-of-organisationregistrationagency-codelist-to-org-id-guide-included-2-03/851>`__)

Activities and Organisations Schemas
-------------------

- Updated definition: all @xml:lang attributes (`#336 <https://github.com/IATI/IATI-Schemas/issues/336>`__) (`discussion link <https://discuss.iatistandard.org/t/language-recommend-use-of-iso-639-1-included-2-03/842>`__)

- Updated definition: [reporting-org, participating-org, receiver-org, provider-org] @ref attribute (`#339 <https://github.com/IATI/IATI-Schemas/issues/339>`__) (`discussion link <https://discuss.iatistandard.org/t/migration-of-organisationregistrationagency-codelist-to-org-id-guide-included-2-03/851>`__)

- Updated definition: reporting-org @secondary-reporter attribute (`#340 <https://github.com/IATI/IATI-Schemas/issues/340>`__) (`discussion link <https://discuss.iatistandard.org/t/modify-definition-of-secondary-publisher-included-2-03/846>`__)

- Updated definition: [recipient-region, recipient-region-budget, sector] @vocabulary-uri attribute (`#341 <https://github.com/IATI/IATI-Schemas/issues/341>`__) (`discussion link <https://discuss.iatistandard.org/t/guidance-on-u-r-i-usage-for-publisher-s-own-vocabularies-included-2-03/850>`__)

- Added new description element (as a child of all document-link elements) (`#357 <https://github.com/IATI/IATI-Schemas/issues/357>`__) (`discussion link <https://discuss.iatistandard.org/t/document-link-description-included-2-03/841>`__)

.. _2_03_codelist_changes:

Codelist Changes
================

A full diff of all **embedded** codelist changes in 2.03 can be found in the `IATI GitHub <https://github.com/IATI/IATI-Codelists/compare/version-2.02...version-2.03#files_bucket>`__

Embedded to Non-Embedded:
------------------------

Alongside 2.03, the following codelists have moved from Embedded to Non-Embedded (`#114 <https://github.com/IATI/IATI-Codelists/issues/114>`__) (`Discussion link <https://discuss.iatistandard.org/t/redefine-selected-codelists-as-non-embedded-included-2-03/854>`__):

.. list-table::
   :widths: 16 16 16
   :header-rows: 0

   * -	ActivityScope
	    -	BudgetIdentifier
	    -	BudgetIdentifierSector-Category
   * -	BudgetIdentifierSector
   	  -	BudgetIdentifierVocabulary
	    -	CRSAddOtherFlags
   * -	ConditionType
	    -	ContactType
	    -	DescriptionType
   * -	DisbursementChannel
   	  -	DocumentCategory-Category
	   	-	GeographicExactness
   *	-	GeographicLocationClass
	   	-	GeographicLocationReach
	   	-	GeographicVocabulary
   *	-	GeographicalPrecision
	   	-	IndicatorMeasure
	   	-	LoanRepaymentPeriod
   *	-	LoanRepaymentType
	   	-	OrganisationType
	   	-	OtherIdentifierType
   *	-	PolicyMarker
	   	-	PolicyMarkerVocabulary
	   	-	PublisherType
   *	-	RegionVocabulary
	   	-	ResultType
	   	-	SectorVocabulary
   *	-	TiedStatus
	   	-	ResultType
	   	-	VerificationStatus
   *	-	PublisherType
	   	-	PolicyMarkerVocabulary
	   	-	PolicyMarker
   *	-	RegionVocabulary
	   	-	TiedStatus
     	- -

New Codelists
-------------

**Non-Embedded:**

- Added AidTypeVocabulary codelist (`#185 <https://github.com/IATI/IATI-Codelists-NonEmbedded/issues/185>`__) (`Discussion link <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__)
- Added BudgetNotProvided codelist (`#184 <https://github.com/IATI/IATI-Codelists-NonEmbedded/issues/184>`__) (`Discussion link <https://discuss.iatistandard.org/t/add-budget-exempt-attribute-and-codelist-included-2-03/845>`__)
- Added ResultVocabulary codelist (`#181 <https://github.com/IATI/IATI-Codelists/issues/181>`__) (`Discussion link <https://discuss.iatistandard.org/t/results-vocabulary-attribute-option-included-2-03/879>`__)
- Added TagVocabulary codelist (`#178 <https://github.com/IATI/IATI-Codelists-NonEmbedded/issues/178>`__) (`Discussion link <https://discuss.iatistandard.org/t/non-statistical-secondary-sectors-excluded-2-03/849>`__)

Updated Codelists
-----------------

**Embedded:**

- TransactionType Codelist (`#112 <https://github.com/IATI/IATI-Codelists/issues/112>`__) (`Discussion link <https://discuss.iatistandard.org/t/transactiontype-codes-included-2-03/852>`__)
 Inlcudes the added codes: Code 12 'Outgoing Pledge' and Code 13 'Incoming Pledge'.

**Non-Embedded:**

- OrganisationType Codelist (`#113 <https://github.com/IATI/IATI-Codelists/issues/113>`__) (`Discussion link <https://discuss.iatistandard.org/t/organisation-type-codes-additions-included-2-03/858>`__)
 Includes the added codes: Code 11 'Local Government', Code 24 'Partner Country based NGO', Code 71 'Private Sector in Provider Country', Code 71 'Private Sector in Aid Recipient Country', Code 73 'Private Sector in Third Country' and Code 90 'Other'.

- IndicatorMeasure codelist (`#179 <https://github.com/IATI/IATI-Codelists-NonEmbedded/issues/179>`__) (`Discussion link <https://discuss.iatistandard.org/t/results-represent-more-than-quantitative-data-included-2-03/872>`__)
 Includes the added codes: Code 3 'Nominal', Code 4 'Ordinal' and Code 5 'Qualitative'.

 .. _2_03_ruleset_changes:

Ruleset Changes
================

A full diff of all Ruleset changes in 2.03 can be found in the `IATI GitHub <https://github.com/IATI/IATI-Codelists/compare/version-2.02...version-2.03#files_bucket>`__

- Added rule: reference element (`#48 <https://github.com/IATI/IATI-Rulesets/issues/48>`__) (`Discussion link <https://discuss.iatistandard.org/t/results-vocabulary-attribute-option-included-2-03/879>`__)

- Added rules: result @value presence - quantitative (`#51 <https://github.com/IATI/IATI-Rulesets/issues/51>`__) (`Discussion link <https://discuss.iatistandard.org/t/results-represent-more-than-quantitative-data-included-2-03/872>`__)

- Added rules: result @value presence - qualitative  (`#52 <https://github.com/IATI/IATI-Rulesets/issues/52>`__) (`Discussion link <https://discuss.iatistandard.org/t/results-represent-more-than-quantitative-data-included-2-03/872>`__)
