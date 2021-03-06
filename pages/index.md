---
title: International Patient Summary Implementation Guide
layout: default
active: home
---

{% include publish-box.html %}


<!-- 
### Jekyll Site Variables

These are the site variables defined [here](http://wiki.hl7.org/index.php?title=IG_Publisher_Documentation#Jekyll):

- IG Business version specification (defined in ig.json)- {% raw %}{{site.data.fhir.ig.version}} {% endraw %} = {{site.data.fhir.ig.version}}

- IG status (defined in ig.xml)- {% raw %}{{site.data.fhir.ig.status}} {% endraw %} = {{site.data.fhir.ig.status}}

- Whether is experimental IG (defined in ig.xml) - {% raw %}{{site.data.fhir.ig.experimental}} {% endraw %} = {{site.data.fhir.ig.experimental}}

- IG Publisher name (defined in ig.xml) - {% raw %}{{site.data.fhir.ig.publisher}} {% endraw %} = {{site.data.fhir.ig.publisher}}

- dependency url - e.g. "uscore" : Base url of a dependency implementation Guide (defined in ig.json) -  {% raw %} {{site.data.fhir.uscore}} {% endraw %}= {{site.data.fhir.uscore}}

- igName : Title of the implementation Guide (defined in ig.xml) -  {% raw %} {{site.data.fhir.igName}} {% endraw %}= {{site.data.fhir.igName}}

- path : path to the main FHIR specification (defined in ig.json)-  {% raw %} {{site.data.fhir.path}} {% endraw %}= {{site.data.fhir.path}}

- canonical : canonical path to this specification (defined in ig.json)-  {% raw %} {{site.data.fhir.canonical}} {% endraw %} = {{site.data.fhir.canonical}}

- errorCount : number of errors in the build file (not including HTML validation errors) -  {% raw %} {{site.data.fhir.errorCount}} {% endraw %} = {{site.data.fhir.errorCount}}

- version : version of FHIR -  {% raw %} {{site.data.fhir.version}} {% endraw %} = {{site.data.fhir.version}}

- revision : revision of FHIR -  {% raw %} {{site.data.fhir.revision}} {% endraw %} = {{site.data.fhir.revision}}

- versionFull : version-revision -  {% raw %} {{site.data.fhir.versionFull}} {% endraw %} = {{site.data.fhir.versionFull}}

- totalFiles : total number of files found by the build -  {% raw %} {{site.data.fhir.totalFiles}} {% endraw %} = {{site.data.fhir.totalFiles}}

- processedFiles : number of files genrated by the build -  {% raw %} {{site.data.fhir.processedFiles}} {% endraw %} = {{site.data.fhir.processedFiles}}

- genDate : date of generation (so date stamps in the pages can match those in the conformance resources) -  {% raw %} {{site.data.fhir.genDate}} {% endraw %} = {{site.data.fhir.genDate}}
-->

# Introduction

An International Patient Summary (IPS) document is an electronic health record extract containing essential healthcare information intended for use in the unscheduled, cross-border care scenario, comprising at least the required elements of the IPS dataset. The IPS dataset is **_a minimal and non-exhaustive patient summary dataset, specialty-agnostic, condition-independent, but readily usable by clinicians for the cross-border unscheduled care of a patient_**.

<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->

## Purpose

The goal of this Implementation Guide is to identify the required clinical data, vocabulary and value sets for an international patient summary. The international patient summary is specified either as templated document using HL7 CDA R2, either as HL7 FHIR composition (described in this guide). The primary use case is to provide support for cross-border or cross-juridictional emergency and unplanned care.

This specification aims to support:

* Cross-jurisdictional patient summaries (through adaptation/extension for multi-language and realm scenarios, including translation).
* Emergency and unplanned care in any country, regardless of language.
* Value sets based on international vocabularies that are usable and understandable in any country.
* Data and metadata for document-level provenance.

## Project Background

See further details on the project background in the IPS Wiki <a href="http://international-patient-summary.net/mediawiki/index.php?title=IPS_Introduction_1#Project_Background">here</a>.

## Project Scope

As expressed in the introduction, the International Patient Summary is:
* a minimal and non-exhaustive patient summary,
* specialty-agnostic,
* condition-independent,
* but readily usable by clinicians for cross-border unscheduled care of a patient.
In this context, minimal and non-exhaustive means that an IPS is not intended to reproduce (the entire) content of an Electronic Health Record (EHR).

Specialty-agnostic means that an IPS is not filtered for a specialty. As an example, allergies are not filtered to the specialty of internal medicine, thus may also include food allergies, if considered to be relevant for, e.g. unplanned care.

Condition-independent means that an IPS is not specific to particular conditions, and focuses on the patient current condition(s).

Furthermore the scope of the IPS is global. Although this is a major challenge, this implementation guide takes various experiences and newer developments into account to address global feasibility as far as possible.

## Relationships with Other Projects and Guidelines

See further details on the IPS project relationships with other projects and guidelines in the IPS Wiki <a href="http://international-patient-summary.net/mediawiki/index.php?title=IPS_implementationguide_1#Relationships_with_other_projects_and_guidelines">here</a>.

## Ballot Status

This Implementation Guide is being balloted as STU with the intention to go normative in a subsequent ballot cycle.


## Authors and Contributors

| Role  | Name | Organization | contact |
| --- | --- | --- | --- |
| **Primary Editor** | Giorgio Cangioli, PhD | Consultant, HL7 Italy | giorgio.cangioli@gmail.com |
| **Primary Editor** | Rob Hausam | Hausam Consulting LLC | rob@hausamconsulting.com |
| **Primary Editor** |  Dr Kai U. Heitmann | Heitmann Consulting and Services, Gefyra GmbH, HL7 Germany | info@kheitmann.de  
| **Primary Editor** | François Macary | Phast | francois.macary@phast.fr |
| **Contributor** | Dr Christof Geßner | Gematik | christof.gessner@gematik.de |
| **Contributor** | Gary Dickinson | CentriHealth | gary.dickinson@ehr-standards.com |
| **Contributor** | Catherine Chronaki | HL7 International Foundation | chronaki@gmail.com |

