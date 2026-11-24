# Quantidade - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0

## Extensão: Quantidade 

**Context of Use**

**Usage info**

**Usos:**

* Usa este Extensão: [Procedimento Realizado](StructureDefinition-BRProcedimentoRealizado-1.0.md)
* Exemplos para este Extensão: [Bundle/example-SA](Bundle-example-SA.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/br.gov.saude.sa.fhir|current/StructureDefinition/StructureDefinition-BRQuantidade-1.0.json)

### Visões formais do conteúdo da extensão

 [Descrição de perfis, diferenciais, instantâneos e suas representações](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

*  [Tabela diferencial](#tabs-diff) 
*  [Tabela de instantâneos](#tabs-snap) 
*  [Estatísticas/Referências](#tabs-summ) 
*  [Todas](#tabs-all) 

Esta estrutura deriva de [Extension](http://hl7.org/fhir/R4/extensibility.html#Extension) 

#### Restrições

Esta estrutura deriva de [Extension](http://hl7.org/fhir/R4/extensibility.html#Extension) 

 **Visão Diferencial** 

Esta estrutura deriva de [Extension](http://hl7.org/fhir/R4/extensibility.html#Extension) 

 **Visão Completa** 

#### Restrições

Esta estrutura deriva de [Extension](http://hl7.org/fhir/R4/extensibility.html#Extension) 

 

Outras representações do perfil: [CSV](../StructureDefinition-BRQuantidade-1.0.csv), [Excel](../StructureDefinition-BRQuantidade-1.0.xlsx), [Schematron](../StructureDefinition-BRQuantidade-1.0.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "BRQuantidade-1.0",
  "meta" : {
    "versionId" : "1",
    "lastUpdated" : "2020-09-17T18:44:06.812+00:00"
  },
  "language" : "pt-BR",
  "url" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BRQuantidade-1.0",
  "version" : "1.0.0",
  "name" : "BRQuantidade",
  "title" : "Quantidade",
  "status" : "active",
  "date" : "2020-09-17T18:44:13.1606848+00:00",
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
  "description" : "Extensão para identificar quantidades.",
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
    "expression" : "Procedure"
  }],
  "type" : "Extension",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Extension",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Extension",
      "path" : "Extension",
      "short" : "Quantidade",
      "definition" : "Identifica quantidades."
    },
    {
      "id" : "Extension.url",
      "path" : "Extension.url",
      "fixedUri" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BRQuantidade-1.0"
    },
    {
      "id" : "Extension.value[x]",
      "path" : "Extension.value[x]",
      "min" : 1,
      "type" : [{
        "code" : "decimal"
      },
      {
        "code" : "integer"
      },
      {
        "code" : "positiveInt"
      },
      {
        "code" : "unsignedInt"
      }]
    }]
  }
}

```
