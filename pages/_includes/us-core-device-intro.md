﻿This profile sets minimum expectations for the [Device] resource to record, search and fetch UDI information associated with a patient. It identifies which core elements, extensions, vocabularies and value sets **SHALL** be present in the resource when using this profile.

**Example Usage Scenarios:**

The following are example usage scenarios for the US Core-Device profile:

-   Query for a Patient's Devices
-   Record a Patient Device

##### Mandatory Data Elements and Terminology


The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation.  Profile specific guidance and examples are provided as well.  The [**Formal Profile Definition**](#profile) below provides the  formal summary, definitions, and  terminology requirements.  

**Each Device must have:**

1.  a UDI string (“udicarrier”)
1.  a code identifying the type of resource
1.  a patient

**Profile specific implementation guidance:**

* none

#### Examples

- [Device-udi-1](Device-udi-1.html)

[Device]: http://hl7.org/fhir/2017Jan/device.html
