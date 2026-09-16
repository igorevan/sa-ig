# Resumo da Evolução Clínica - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Resource Profile: Resumo da Evolução Clínica 

 
Descrição da evolução clínica do indivíduo. 

**Usos:**

* Refere a este Perfil: [Sumário de Alta (SA)](StructureDefinition-BRSumarioAlta.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/br.gov.saude.sa.fhir|current/StructureDefinition/StructureDefinition-BRResumoEvolucaoClinica.json)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-BRResumoEvolucaoClinica.csv), [Excel](../StructureDefinition-BRResumoEvolucaoClinica.xlsx), [Schematron](../StructureDefinition-BRResumoEvolucaoClinica.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "BRResumoEvolucaoClinica",
  "extension" : [{
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-wg",
    "valueCode" : "ehr"
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-fmm",
    "valueInteger" : 1,
    "_valueInteger" : {
      "extension" : [{
        "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-conformance-derivedFrom",
        "valueCanonical" : "https://fhir.saude.gov.br/sa/ImplementationGuide/br.gov.saude.sa.fhir"
      }]
    }
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
    "valueCode" : "normative",
    "_valueCode" : {
      "extension" : [{
        "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-conformance-derivedFrom",
        "valueCanonical" : "https://fhir.saude.gov.br/sa/ImplementationGuide/br.gov.saude.sa.fhir"
      }]
    }
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-normative-version",
    "valueCode" : "4.0.1"
  }],
  "url" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BRResumoEvolucaoClinica",
  "version" : "1.0.0-release",
  "name" : "BRResumoEvolucaoClinica",
  "title" : "Resumo da Evolução Clínica",
  "status" : "active",
  "date" : "2024-05-15T02:15:49.3292398+00:00",
  "publisher" : "Ministério da Saúde do Brasil",
  "contact" : [{
    "name" : "Ministério da Saúde do Brasil",
    "telecom" : [{
      "system" : "url",
      "value" : "http://www.saude.gov.br"
    },
    {
      "system" : "email",
      "value" : "cgiis.datasus@saude.gov.br"
    }]
  }],
  "description" : "Descrição da evolução clínica do indivíduo.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "BR"
    }]
  }],
  "fhirVersion" : "4.0.1",
  "mapping" : [{
    "identity" : "workflow",
    "uri" : "http://hl7.org/fhir/workflow",
    "name" : "Workflow Pattern"
  },
  {
    "identity" : "v2",
    "uri" : "http://hl7.org/v2",
    "name" : "HL7 v2 Mapping"
  },
  {
    "identity" : "w5",
    "uri" : "http://hl7.org/fhir/fivews",
    "name" : "FiveWs Pattern Mapping"
  },
  {
    "identity" : "rim",
    "uri" : "http://hl7.org/v3",
    "name" : "RIM Mapping"
  }],
  "kind" : "resource",
  "abstract" : false,
  "type" : "ClinicalImpression",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/ClinicalImpression",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "ClinicalImpression",
      "path" : "ClinicalImpression"
    },
    {
      "id" : "ClinicalImpression.identifier",
      "path" : "ClinicalImpression.identifier",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.status",
      "path" : "ClinicalImpression.status",
      "fixedCode" : "completed"
    },
    {
      "id" : "ClinicalImpression.statusReason",
      "path" : "ClinicalImpression.statusReason",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.code",
      "path" : "ClinicalImpression.code",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.description",
      "path" : "ClinicalImpression.description",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.subject",
      "path" : "ClinicalImpression.subject",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRIndividuo-1.0"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "ClinicalImpression.subject.reference",
      "path" : "ClinicalImpression.subject.reference",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.subject.type",
      "path" : "ClinicalImpression.subject.type",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.subject.identifier.use",
      "path" : "ClinicalImpression.subject.identifier.use",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.subject.identifier.type",
      "path" : "ClinicalImpression.subject.identifier.type",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.subject.identifier.system",
      "path" : "ClinicalImpression.subject.identifier.system",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "ClinicalImpression.subject.identifier.value",
      "path" : "ClinicalImpression.subject.identifier.value",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "ClinicalImpression.subject.identifier.period",
      "path" : "ClinicalImpression.subject.identifier.period",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.subject.identifier.assigner",
      "path" : "ClinicalImpression.subject.identifier.assigner",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.subject.display",
      "path" : "ClinicalImpression.subject.display",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.encounter",
      "path" : "ClinicalImpression.encounter",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.effective[x]",
      "path" : "ClinicalImpression.effective[x]",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.date",
      "path" : "ClinicalImpression.date",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.assessor",
      "path" : "ClinicalImpression.assessor",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.previous",
      "path" : "ClinicalImpression.previous",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.problem",
      "path" : "ClinicalImpression.problem",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.investigation",
      "path" : "ClinicalImpression.investigation",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.protocol",
      "path" : "ClinicalImpression.protocol",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.summary",
      "path" : "ClinicalImpression.summary",
      "short" : "Resumo da evolução clínica",
      "definition" : "Descrição da evolução clínica do indivíduo.",
      "min" : 1,
      "mapping" : [{
        "identity" : "rnds",
        "map" : "SA.6.1"
      }]
    },
    {
      "id" : "ClinicalImpression.finding",
      "path" : "ClinicalImpression.finding",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.prognosisCodeableConcept",
      "path" : "ClinicalImpression.prognosisCodeableConcept",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.prognosisReference",
      "path" : "ClinicalImpression.prognosisReference",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.supportingInfo",
      "path" : "ClinicalImpression.supportingInfo",
      "max" : "0"
    },
    {
      "id" : "ClinicalImpression.note",
      "path" : "ClinicalImpression.note",
      "max" : "0"
    }]
  }
}

```
