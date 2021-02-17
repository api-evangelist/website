---
published: true
layout: post
title: 'Creating A Postman Collection For The Fast Healthcare Interoperability Resources (FHIR) Specification'
image: https://kinlane-productions2.s3.amazonaws.com/fhir/fhir-specification-screenshot.png
---
<p><img style="padding: 15px;" src="https://kinlane-productions2.s3.amazonaws.com/fhir/fhir-specification-screenshot.png" alt="" width="40%" align="right" /></p>
<p>I have been working on healthcare APIs in government for over five  years now, providing feedback regularly to the Blue Button API effort  over at Health and Human Service (HHS), <a href="http://apievangelist.com/2018/09/18/talking-healthcare-apis-with-the-cms-blue-button-api-team-at-apistrat-in/">including having them speak at APIStrat last year in Nashville</a>, and <a href="http://apievangelist.com/2018/09/18/talking-healthcare-apis-with-the-cms-blue-button-api-team-at-apistrat-in/">me speaking at the White House as part of the Blue Button 2.0 summit</a>.  I&rsquo;m always looking for more ways that I can contribute to the  healthcare API ecosystem, especially when it comes to investing in <a href="https://www.fhir.org/">the Fast Healthcare Interoperability Resources (FHIR) specification</a>.  Now that I have bandwidth to invest in healthcare APIs again, I wanted  to get my mind thinking about the potential of the FHIR specification,  and find ways to help move the conversation forward.<br /><br />To jumpstart my work on the Fast Healthcare Interoperability Resources (FHIR) specification I generated <a href="https://www.postman.com/collections/28f36ef9615b6e5b13b7">a Postman Collection</a> from the FHIR test server, reverse engineering the specification and  creating my first draft of a collection to center my effort around. The  Postman Collection covers the following resource types:</p>
<table>
<tbody>
<tr>
<td width="25%" valign="top">
<ul>
<li> Account </li>
<li> ActivityDefinition </li>
<li> AdverseEvent </li>
<li> AllergyIntolerance </li>
<li> Appointment </li>
<li> AppointmentResponse </li>
<li> AuditEvent </li>
<li> Basic </li>
<li> Binary </li>
<li> BiologicallyDerivedProduct </li>
<li> BodyStructure </li>
<li> Bundle </li>
<li> CapabilityStatement </li>
<li> CarePlan </li>
<li> CareTeam </li>
<li> CatalogEntry </li>
<li> ChargeItem </li>
<li> ChargeItemDefinition </li>
<li> Claim </li>
<li> ClaimResponse </li>
<li> ClinicalImpression </li>
<li> CodeSystem </li>
<li> Communication </li>
<li> CommunicationRequest </li>
<li> CompartmentDefinition </li>
<li> Composition </li>
<li> ConceptMap </li>
<li> Condition </li>
<li> Consent </li>
<li> Contract </li>
<li> Coverage </li>
<li> CoverageEligibilityRequest </li>
<li> CoverageEligibilityResponse </li>
<li> DetectedIssue </li>
<li> Device </li>
<li> DeviceDefinition </li>
</ul>
</td>
<td width="25%" valign="top">
<ul>
<li> DeviceMetric </li>
<li> DeviceRequest </li>
<li> DeviceUseStatement </li>
<li> DiagnosticReport </li>
<li> DocumentManifest </li>
<li> DocumentReference </li>
<li> EffectEvidenceSynthesis </li>
<li> Encounter </li>
<li> Endpoint </li>
<li> EnrollmentRequest </li>
<li> EnrollmentResponse </li>
<li> EpisodeOfCare </li>
<li> EventDefinition </li>
<li> Evidence </li>
<li> EvidenceVariable </li>
<li> ExampleScenario </li>
<li> ExplanationOfBenefit </li>
<li> FamilyMemberHistory </li>
<li> Flag </li>
<li> Goal </li>
<li> GraphDefinition </li>
<li> Group </li>
<li> GuidanceResponse </li>
<li> HealthcareService </li>
<li> ImagingStudy </li>
<li> Immunization </li>
<li> ImmunizationEvaluation </li>
<li> ImmunizationRecommendation </li>
<li> ImplementationGuide </li>
<li> InsurancePlan </li>
<li> Invoice </li>
<li> Library </li>
<li> Linkage </li>
<li> List </li>
<li> Location </li>
<li> Measure </li>
</ul>
</td>
<td width="25%" valign="top">
<ul>
<li> MeasureReport </li>
<li> Media </li>
<li> Medication </li>
<li> MedicationAdministration </li>
<li> MedicationDispense </li>
<li> MedicationKnowledge </li>
<li> MedicationRequest </li>
<li> MedicationStatement </li>
<li> MedicinalProduct </li>
<li> MedicinalProductAuthorization </li>
<li> MedicinalProductContraindication </li>
<li> MedicinalProductIndication </li>
<li> MedicinalProductIngredient </li>
<li> MedicinalProductInteraction </li>
<li> MedicinalProductManufactured </li>
<li> MedicinalProductPackaged </li>
<li> MedicinalProductPharmaceutical </li>
<li> MedicinalProductUndesirableEffect </li>
<li> MessageDefinition </li>
<li> MessageHeader </li>
<li> MolecularSequence </li>
<li> NamingSystem </li>
<li> NutritionOrder </li>
<li> Observation </li>
<li> ObservationDefinition </li>
<li> OperationDefinition </li>
<li> OperationOutcome </li>
<li> Organization </li>
<li> OrganizationAffiliation </li>
<li> Parameters </li>
<li> Patient </li>
<li> PaymentNotice </li>
<li> PaymentReconciliation </li>
<li> Person </li>
<li> PlanDefinition </li>
<li> Practitioner </li>
</ul>
</td>
<td width="25%" valign="top">
<ul>
<li> PractitionerRole </li>
<li> Procedure </li>
<li> Provenance </li>
<li> Questionnaire </li>
<li> QuestionnaireResponse </li>
<li> RelatedPerson </li>
<li> RequestGroup </li>
<li> ResearchDefinition </li>
<li> ResearchElementDefinition </li>
<li> ResearchStudy </li>
<li> ResearchSubject </li>
<li> RiskAssessment </li>
<li> RiskEvidenceSynthesis </li>
<li> Schedule </li>
<li> SearchParameter </li>
<li> ServiceRequest </li>
<li> Slot </li>
<li> Specimen </li>
<li> SpecimenDefinition </li>
<li> StructureDefinition </li>
<li> StructureMap </li>
<li> Subscription </li>
<li> Substance </li>
<li> SubstanceSpecification </li>
<li> SupplyDelivery </li>
<li> SupplyRequest </li>
<li> Task </li>
<li> TerminologyCapabilities </li>
<li> TestReport </li>
<li> TestScript </li>
<li> ValueSet </li>
<li> VerificationResult </li>
<li> VisionPrescription </li>
</ul>
</td>
</tr>
</tbody>
</table>
<p><a href="http://test.fhir.org/r4">The FHIR API specification collection points at the FHIR test server by default</a>,  and some of the paths need parameters dialed in a little better to  work. Next I&rsquo;ll work on cleaning up the ecollection some, making sure  the properties have descriptions, and every request has examples  defined. Then I&rsquo;ll publish some documentation and a FHIR API mock  server. Once I get to this point I&rsquo;ll look at defining an environment,  as well as tests that cover the entire surface area for all resource  types. Rounding off the FHIR Postman collection a little more, making  sure it isn&rsquo;t just a definition, but a contract that can be used to  certify any FHIR API deployment.<br /><br />I am looking to refresh my FHIR  knowledge using the most recent 4.0 version of the healthcare  specification, while also evolving my storytelling around how to define  API contracts that can be applied to APIs spanning an entire industry.  I&rsquo;d say that the FHIR specification is the most important API definition  we have right now. It is the most sophisticated openly defined industry  schema that has both government and industry support, supportsing  critical deployments like the Blue Button API for Medicare and the  Department of Veterans Affairs, and is something that has the potential  to impact millions of people. It&rsquo;s a relevant API, and something I want  to continue helping evangelize and invest in the API specification as  part of my work with Postman.</p>
