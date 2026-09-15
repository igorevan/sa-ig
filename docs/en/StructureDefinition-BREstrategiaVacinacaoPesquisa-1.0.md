# Estratégia de Vacinação Pesquisa - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Extension: Estratégia de Vacinação Pesquisa 

Extensão para as informações relacionadas aos dados da pesquisa clínica registrada na ANVISA.

**Context of Use**

**Usage info**

**Usos:**

* Usa este Extensão: [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)
* Exemplos para este Extensão: [Bundle/example-RIA-R](Bundle-example-RIA-R.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/br.gov.saude.sa.fhir|current/StructureDefinition/StructureDefinition-BREstrategiaVacinacaoPesquisa-1.0.json)

### Formal Views of Extension Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-BREstrategiaVacinacaoPesquisa-1.0.csv), [Excel](../StructureDefinition-BREstrategiaVacinacaoPesquisa-1.0.xlsx), [Schematron](../StructureDefinition-BREstrategiaVacinacaoPesquisa-1.0.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "BREstrategiaVacinacaoPesquisa-1.0",
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
  "url" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BREstrategiaVacinacaoPesquisa-1.0",
  "version" : "1.0.0-release",
  "name" : "BREstrategiaVacinacaoPesquisa",
  "title" : "Estratégia de Vacinação Pesquisa",
  "status" : "active",
  "date" : "2021-09-03",
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
  "description" : "Extensão para as informações relacionadas aos dados da pesquisa clínica registrada na ANVISA.",
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
    "expression" : "Immunization.protocolApplied"
  }],
  "type" : "Extension",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Extension",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Extension",
      "path" : "Extension",
      "short" : "Estrategia de Vacinacao Pesquisa",
      "definition" : "Extensão para as informações relacionadas aos dados da pesquisa clínica registrada na ANVISA.",
      "alias" : ["Pesquisa Clínica"],
      "mustSupport" : false
    },
    {
      "id" : "Extension.extension:numeroProtocoloEstudoANVISA",
      "path" : "Extension.extension",
      "sliceName" : "numeroProtocoloEstudoANVISA",
      "label" : "Anvisa Protocolo Estudo",
      "short" : "Anvisa Protocolo Estudo",
      "definition" : "Número do protocolo do estudo clínico na Anvisa.",
      "max" : "1"
    },
    {
      "id" : "Extension.extension:numeroProtocoloEstudoANVISA.url",
      "path" : "Extension.extension.url",
      "fixedUri" : "numeroProtocoloEstudoANVISA"
    },
    {
      "id" : "Extension.extension:numeroProtocoloEstudoANVISA.value[x]",
      "path" : "Extension.extension.value[x]",
      "min" : 1,
      "type" : [{
        "code" : "string"
      }]
    },
    {
      "id" : "Extension.extension:numeroVersaoProtocoloEstudo",
      "path" : "Extension.extension",
      "sliceName" : "numeroVersaoProtocoloEstudo",
      "label" : "Anvisa Protocolo Versão",
      "short" : "Anvisa Protocolo Versão",
      "definition" : "Número da versão do protocolo do estudo na Anvisa.",
      "max" : "1"
    },
    {
      "id" : "Extension.extension:numeroVersaoProtocoloEstudo.url",
      "path" : "Extension.extension.url",
      "fixedUri" : "numeroVersaoProtocoloEstudo"
    },
    {
      "id" : "Extension.extension:numeroVersaoProtocoloEstudo.value[x]",
      "path" : "Extension.extension.value[x]",
      "min" : 1,
      "type" : [{
        "code" : "string"
      }]
    },
    {
      "id" : "Extension.extension:numeroRegistroVacinaAnvisa",
      "path" : "Extension.extension",
      "sliceName" : "numeroRegistroVacinaAnvisa",
      "label" : "Anvisa Num Registro",
      "short" : "Anvisa Num Registro",
      "definition" : "Número do registro sanitário da vacina na Anvisa, seja este registro emergencial ou definitivo.",
      "max" : "1"
    },
    {
      "id" : "Extension.extension:numeroRegistroVacinaAnvisa.url",
      "path" : "Extension.extension.url",
      "fixedUri" : "numeroRegistroVacinaAnvisa"
    },
    {
      "id" : "Extension.extension:numeroRegistroVacinaAnvisa.value[x]",
      "path" : "Extension.extension.value[x]",
      "min" : 1,
      "type" : [{
        "code" : "string"
      }]
    },
    {
      "id" : "Extension.url",
      "path" : "Extension.url",
      "fixedUri" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BREstrategiaVacinacaoPesquisa-1.0"
    },
    {
      "id" : "Extension.value[x]",
      "path" : "Extension.value[x]",
      "max" : "0"
    }]
  }
}

```
