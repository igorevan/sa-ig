# Restrições Funcionais e Incapacidades em Saúde - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Resource Profile: Restrições Funcionais e Incapacidades em Saúde 

 
Registra restrições funcionais ou incapacidades em saúde observadas no indivíduo. 

**Usos:**

* Refere a este Perfil: [Sumário de Alta (SA)](StructureDefinition-BRSumarioAlta.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/br.gov.saude.sa.fhir|current/StructureDefinition/StructureDefinition-BRRestricaoFuncionalIncapacidadeSaude-1.0.json)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-BRRestricaoFuncionalIncapacidadeSaude-1.0.csv), [Excel](../StructureDefinition-BRRestricaoFuncionalIncapacidadeSaude-1.0.xlsx), [Schematron](../StructureDefinition-BRRestricaoFuncionalIncapacidadeSaude-1.0.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "BRRestricaoFuncionalIncapacidadeSaude-1.0",
  "meta" : {
    "versionId" : "1",
    "lastUpdated" : "2024-05-22T10:43:32.4929465+00:00"
  },
  "language" : "pt-BR",
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
  "url" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BRRestricaoFuncionalIncapacidadeSaude-1.0",
  "version" : "1.0.0-release",
  "name" : "BRRestricaoFuncionalIncapacidadeSaude",
  "title" : "Restrições Funcionais e Incapacidades em Saúde",
  "status" : "active",
  "experimental" : false,
  "date" : "2020-09-20T20:14:54.4843666+00:00",
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
  "description" : "Registra restrições funcionais ou incapacidades em saúde observadas no indivíduo.",
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
    "identity" : "sct-concept",
    "uri" : "http://snomed.info/conceptdomain",
    "name" : "SNOMED CT Concept Domain Binding"
  },
  {
    "identity" : "v2",
    "uri" : "http://hl7.org/v2",
    "name" : "HL7 v2 Mapping"
  },
  {
    "identity" : "rim",
    "uri" : "http://hl7.org/v3",
    "name" : "RIM Mapping"
  },
  {
    "identity" : "w5",
    "uri" : "http://hl7.org/fhir/fivews",
    "name" : "FiveWs Pattern Mapping"
  },
  {
    "identity" : "sct-attr",
    "uri" : "http://snomed.org/attributebinding",
    "name" : "SNOMED CT Attribute Binding"
  }],
  "kind" : "resource",
  "abstract" : false,
  "type" : "Condition",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Condition",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Condition",
      "path" : "Condition",
      "short" : "Restrições Funcionais e Incapacidades em Saúde",
      "definition" : "Registra restrições funcionais ou incapacidades em saúde observadas no indivíduo.",
      "mustSupport" : false
    },
    {
      "id" : "Condition.identifier",
      "path" : "Condition.identifier",
      "max" : "0"
    },
    {
      "id" : "Condition.clinicalStatus",
      "path" : "Condition.clinicalStatus",
      "short" : "Status da Restrição Funcional ou Incapacidade",
      "definition" : "O estado clínico da condição.",
      "min" : 1,
      "mustSupport" : false,
      "binding" : {
        "strength" : "required",
        "description" : "Estado da Restrição Funcional ou Incapacidade de Saúde",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BREstadoRestricaoFuncionalIncapacidadeSaude-1.0"
      },
      "mapping" : [{
        "identity" : "rnds",
        "map" : "SA.4.2"
      }]
    },
    {
      "id" : "Condition.clinicalStatus.coding",
      "path" : "Condition.clinicalStatus.coding",
      "max" : "1"
    },
    {
      "id" : "Condition.clinicalStatus.coding.system",
      "path" : "Condition.clinicalStatus.coding.system",
      "min" : 1
    },
    {
      "id" : "Condition.clinicalStatus.coding.version",
      "path" : "Condition.clinicalStatus.coding.version",
      "max" : "0"
    },
    {
      "id" : "Condition.clinicalStatus.coding.code",
      "path" : "Condition.clinicalStatus.coding.code",
      "min" : 1,
      "mapping" : [{
        "identity" : "rnds",
        "map" : "SA.4.2"
      }]
    },
    {
      "id" : "Condition.clinicalStatus.coding.userSelected",
      "path" : "Condition.clinicalStatus.coding.userSelected",
      "max" : "0"
    },
    {
      "id" : "Condition.clinicalStatus.text",
      "path" : "Condition.clinicalStatus.text",
      "max" : "0"
    },
    {
      "id" : "Condition.verificationStatus",
      "path" : "Condition.verificationStatus",
      "max" : "0"
    },
    {
      "id" : "Condition.category",
      "path" : "Condition.category",
      "max" : "0"
    },
    {
      "id" : "Condition.severity",
      "path" : "Condition.severity",
      "max" : "0"
    },
    {
      "id" : "Condition.code",
      "path" : "Condition.code",
      "short" : "Restrição Funcional ou Incapacidade",
      "definition" : "Identificação da restrição funcional ou incapacidade em saúde.",
      "min" : 1,
      "mustSupport" : true,
      "mapping" : [{
        "identity" : "rnds",
        "map" : "SA.4.1"
      }]
    },
    {
      "id" : "Condition.code.coding",
      "path" : "Condition.code.coding",
      "max" : "0"
    },
    {
      "id" : "Condition.code.coding.display",
      "path" : "Condition.code.coding.display",
      "max" : "0"
    },
    {
      "id" : "Condition.code.coding.userSelected",
      "path" : "Condition.code.coding.userSelected",
      "max" : "0"
    },
    {
      "id" : "Condition.code.text",
      "path" : "Condition.code.text",
      "short" : "Representação em Texto Livre do Conceito",
      "definition" : "Representação em linguagem natural do conceito como visto/selecionado/enviado pelo usuário que registrou a informação e/ou que representa o significado da intenção do usuário.",
      "min" : 1,
      "mapping" : [{
        "identity" : "rnds",
        "map" : "SA.4.1"
      }]
    },
    {
      "id" : "Condition.bodySite",
      "path" : "Condition.bodySite",
      "max" : "0"
    },
    {
      "id" : "Condition.subject",
      "path" : "Condition.subject",
      "short" : "Indivíduo com a restrição funcional e/ou incapacidade em saúde",
      "definition" : "Indica o paciente ou grupo o qual tem a restrição funcional e/ou incapacidade em saúde registrada.",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRIndividuo-1.0"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "Condition.subject.id",
      "path" : "Condition.subject.id",
      "max" : "0"
    },
    {
      "id" : "Condition.subject.reference",
      "path" : "Condition.subject.reference",
      "max" : "0"
    },
    {
      "id" : "Condition.subject.type",
      "path" : "Condition.subject.type",
      "max" : "0"
    },
    {
      "id" : "Condition.subject.identifier",
      "path" : "Condition.subject.identifier",
      "min" : 1
    },
    {
      "id" : "Condition.subject.identifier.use",
      "path" : "Condition.subject.identifier.use",
      "max" : "0"
    },
    {
      "id" : "Condition.subject.identifier.type",
      "path" : "Condition.subject.identifier.type",
      "max" : "0"
    },
    {
      "id" : "Condition.subject.identifier.system",
      "path" : "Condition.subject.identifier.system",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "Condition.subject.identifier.value",
      "path" : "Condition.subject.identifier.value",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "Condition.subject.identifier.period",
      "path" : "Condition.subject.identifier.period",
      "max" : "0"
    },
    {
      "id" : "Condition.subject.identifier.assigner",
      "path" : "Condition.subject.identifier.assigner",
      "max" : "0"
    },
    {
      "id" : "Condition.subject.display",
      "path" : "Condition.subject.display",
      "max" : "0"
    },
    {
      "id" : "Condition.encounter",
      "path" : "Condition.encounter",
      "max" : "0"
    },
    {
      "id" : "Condition.onset[x]",
      "path" : "Condition.onset[x]",
      "max" : "0"
    },
    {
      "id" : "Condition.abatement[x]",
      "path" : "Condition.abatement[x]",
      "max" : "0"
    },
    {
      "id" : "Condition.recordedDate",
      "path" : "Condition.recordedDate",
      "max" : "0"
    },
    {
      "id" : "Condition.recorder",
      "path" : "Condition.recorder",
      "max" : "0"
    },
    {
      "id" : "Condition.asserter",
      "path" : "Condition.asserter",
      "max" : "0"
    },
    {
      "id" : "Condition.stage",
      "path" : "Condition.stage",
      "max" : "0"
    },
    {
      "id" : "Condition.evidence",
      "path" : "Condition.evidence",
      "max" : "0"
    },
    {
      "id" : "Condition.note",
      "path" : "Condition.note",
      "max" : "0"
    }]
  }
}

```
