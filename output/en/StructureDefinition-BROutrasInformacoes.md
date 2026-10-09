# Outras Informações - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Extension: Outras Informações 

**Context of Use**

**Usage info**

**Usos:**

* Usa este Extensão: [Contato Assistencial](StructureDefinition-BRContatoAssistencial-1.0.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/br.gov.saude.sa.fhir|current/StructureDefinition/StructureDefinition-BROutrasInformacoes.json)

### Formal Views of Extension Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-BROutrasInformacoes.csv), [Excel](../StructureDefinition-BROutrasInformacoes.xlsx), [Schematron](../StructureDefinition-BROutrasInformacoes.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "BROutrasInformacoes",
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
  "url" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BROutrasInformacoes",
  "version" : "1.0.0-release",
  "name" : "BROutrasInformacoes",
  "title" : "Outras Informações",
  "status" : "active",
  "date" : "2022-05-26",
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
  "description" : "Representa quaisquer outras informações acerca dos dados de desfecho do atendimento registrado.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "BR"
    }]
  }],
  "fhirVersion" : "4.0.1",
  "mapping" : [{
    "identity" : "rim",
    "uri" : "http://hl7.org/v3",
    "name" : "RIM Mapping"
  }],
  "kind" : "complex-type",
  "abstract" : false,
  "context" : [{
    "type" : "element",
    "expression" : "Encounter.hospitalization"
  }],
  "type" : "Extension",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Extension",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Extension.url",
      "path" : "Extension.url",
      "fixedUri" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BROutrasInformacoes"
    },
    {
      "id" : "Extension.value[x]",
      "path" : "Extension.value[x]",
      "type" : [{
        "code" : "Annotation"
      }]
    }]
  }
}

```
