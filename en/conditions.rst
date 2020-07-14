Conditions
==========

IATI asks publishers to declare any conditions or specific terms that are attached to their activities. For example, these could be the requirements issued by a funder or a six month review to assess whether or not the activity is worth continuing.

Definition
----------
Within the **IATI activity standard** conditions that relate to an ``iati-activity`` can be described:

* ``conditions`` - a container element to declare whether ``condition`` are attached.
* ``condition`` - the specific statement around a condition.


Considerations
--------------
When using the **IATI activity standard** to declare *conditions*, the following should be considered:

* An ``iati-activity`` does not require a ``conditions`` statement, if none are relevant.
* However, it is also valid to declare that no ``conditions`` are attached to a specific ``iati-activity`` via the ``@attached`` attribute.
* For every ``condition`` a relevant *ConditionType* code is expected.
* When multiple ``condition`` exist, these can be presented separately within the same ``conditions`` element.
* The same ``condition`` can be presented in different languages, by using the ``narrative`` child element`` and the relevant *xml:lang*.
* The free-text to describe the condition should avoid jargon

2.01+ Considerations
--------------------
In versions 2.01 and above, the following must also be considered:

* Any freetext condition text must be included in the child ``narrative`` element, which can be repeated for different languages.

.. meta::
  :title: Conditions
  :description: IATI asks publishers to declare any conditions or specific terms that are attached to their activities.
  :guidance_type: activity
  :date: October 15, 2015
