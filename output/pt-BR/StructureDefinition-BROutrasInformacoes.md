# Outras Informações - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0

## Extensão: Outras Informações 

**Context of Use**

**Usage info**

**Usos:**

* Usa este Extensão: [Contato Assistencial](StructureDefinition-BRContatoAssistencial-1.0.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/br.gov.saude.sa.fhir|current/StructureDefinition/StructureDefinition-BROutrasInformacoes.json)

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

 

Outras representações do perfil: [CSV](../StructureDefinition-BROutrasInformacoes.csv), [Excel](../StructureDefinition-BROutrasInformacoes.xlsx), [Schematron](../StructureDefinition-BROutrasInformacoes.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "BROutrasInformacoes",
  "url" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BROutrasInformacoes",
  "version" : "1.0.0",
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
