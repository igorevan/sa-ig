# Estado da Restrição Funcional ou Incapacidade de Saúde - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## ValueSet: Estado da Restrição Funcional ou Incapacidade de Saúde 

 
Estado da Restrição Funcional ou Incapacidade de Saúde 

 **References** 

* [Restrições Funcionais e Incapacidades em Saúde](StructureDefinition-BRRestricaoFuncionalIncapacidadeSaude-1.0.md)

### Logical Definition (CLD)

 

### Expansion

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "BREstadoRestricaoFuncionalIncapacidadeSaude-1.0",
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
  "url" : "http://www.saude.gov.br/fhir/r4/ValueSet/BREstadoRestricaoFuncionalIncapacidadeSaude-1.0",
  "version" : "1.0.0-release",
  "name" : "BREstadoRestricaoFuncionalIncapacidadeSaude",
  "title" : "Estado da Restrição Funcional ou Incapacidade de Saúde",
  "status" : "active",
  "experimental" : false,
  "date" : "2020-09-20T20:16:27.4283634+00:00",
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
  "description" : "Estado da Restrição Funcional ou Incapacidade de Saúde",
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
        "code" : "inactive",
        "designation" : [{
          "language" : "pt-BR",
          "value" : "Inativo"
        }]
      }]
    }]
  }
}

```
