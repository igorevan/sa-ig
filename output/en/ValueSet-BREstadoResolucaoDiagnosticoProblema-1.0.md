# Estado da Resolução de Diagnóstico ou Problema - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## ValueSet: Estado da Resolução de Diagnóstico ou Problema 

 
Estado da resolução de um diagnóstico ou problema. 

 **References** 

* [CID10 Avaliado](StructureDefinition-BRCID10Avaliado-1.0.md)

### Logical Definition (CLD)

 

### Expansion

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "BREstadoResolucaoDiagnosticoProblema-1.0",
  "language" : "en",
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
  "url" : "http://www.saude.gov.br/fhir/r4/ValueSet/BREstadoResolucaoDiagnosticoProblema-1.0",
  "version" : "1.0.0-release",
  "name" : "BREstadoResolucaoDiagnosticoProblema",
  "title" : "Estado da Resolução de Diagnóstico ou Problema",
  "status" : "active",
  "experimental" : false,
  "date" : "2020-03-12T13:09:53.3447193+00:00",
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
  "description" : "Estado da resolução de um diagnóstico ou problema.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "BR"
    }]
  }],
  "immutable" : false,
  "compose" : {
    "include" : [{
      "system" : "http://terminology.hl7.org/CodeSystem/condition-clinical",
      "concept" : [{
        "code" : "active",
        "designation" : [{
          "language" : "pt-BR",
          "value" : "Ativo"
        }]
      },
      {
        "code" : "recurrence",
        "designation" : [{
          "language" : "pt-BR",
          "value" : "Recorrente"
        }]
      },
      {
        "code" : "relapse",
        "designation" : [{
          "language" : "pt-BR",
          "value" : "Recidiva"
        }]
      },
      {
        "code" : "inactive",
        "designation" : [{
          "language" : "pt-BR",
          "value" : "Inativo"
        }]
      },
      {
        "code" : "remission",
        "designation" : [{
          "language" : "pt-BR",
          "value" : "Remissão"
        }]
      },
      {
        "code" : "resolved",
        "designation" : [{
          "language" : "pt-BR",
          "value" : "Resolvido"
        }]
      }]
    }]
  }
}

```
