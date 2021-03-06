Both the [MedicationRequest] and [MedicationStatement] resources can be used to record a patient's medication.  For more information about the context for their usages, refer to the medication domains's [boundaries section].  This profile sets minimum expectations for the MedicationStatement resource to record, search and fetch medications associated with a patient. It identifies which core elements, extensions, vocabularies and value sets **SHALL** be present in the resource when using this profile.

**Example Usage Scenarios:**

The following are example usage scenarios for the
US Core-MedicationStatement profile:

-   Record or Query active medications being taken by a patient

##### Mandatory Data Elements and Terminology


The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation.  Profile specific guidance and examples are provided as well.  The [**Formal Profile Definition**](#profile) below provides the  formal summary, definitions, and  terminology requirements.  

**Each MedicationStatement must have:**

1.  a status
1.  a medication
1.  a patient
1.  a date



**Profile specific implementation guidance:**

*  The MedicationStatement and MedicationRequest resources can represent a medication, using either a code or refer to a [Medication] resource.
    *  When referencing a Medication resource,  the resource may be [contained] or an external resource.
    *  The server application can choose any one way or more than one method,  but if the an external reference to Medication is used, the server SHALL support the [include] parameter for searching this element.
    *  The client application must support both methods.  
    *  Additional guidance is provided below in the Search section and in the [CapabilityStatement] section.

#### Examples

- [MedicationStatement-uscore-ms1](MedicationStatement-uscore-ms1.html) This example uses an inline medication code to represent the medication.
- [MedicationStatement-uscore-ms2](MedicationStatement-uscore-ms2.html)  This example references a [contained](http://hl7.org/fhir/2017Jan/references.html#contained) Medication resource.
- [MedicationStatement-uscore-ms3](Bundle-uscore-ms3.html) This example is a search [Bundle](http://hl7.org/fhir/2017Jan/bundle.html) with a MedicationStatement and an included Medication resource in the Bundle.

  [Medication Clinical Drug (RxNorm)]: ValueSet-us-core-medication-codes.html
  [MedicationRequestStatus]: http://hl7.org/fhir/us/daf/ValueSet-medication-request-status.html
[MedicationStatementStatus]: http://hl7.org/fhir/us/daf/ValueSet-medication-statement-status.html
[MedicationStatement]:http://hl7.org/fhir/2017Jan/medicationstatement.html
 [MedicationRequest]: http://hl7.org/fhir/2017Jan/medicationrequest.html
 [Medication]:http://hl7.org/fhir/2017Jan/medication.html
 [CapabilityStatement]: capstmnts.html
 [boundaries section]: http://hl7.org/fhir/2017Jan/medicationrequest.html#bnr
[include]: http://hl7.org/fhir/2017Jan/search.html#include
[contained]: http://hl7.org/fhir/2017Jan/references.html#contained
