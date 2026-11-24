# Estado da Restrição Funcional ou Incapacidade de Saúde - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0

## ValueSet: Estado da Restrição Funcional ou Incapacidade de Saúde 

 **References** 

* [Restrições Funcionais e Incapacidades em Saúde](StructureDefinition-BRRestricaoFuncionalIncapacidadeSaude-1.0.md)

### Definição lógica (CLD)

 

### Expansão

-------

 [Descrição do(s) quadro(s) acima](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "BREstadoRestricaoFuncionalIncapacidadeSaude-1.0",
  "language" : "en",
  "url" : "http://www.saude.gov.br/fhir/r4/ValueSet/BREstadoRestricaoFuncionalIncapacidadeSaude-1.0",
  "version" : "1.0.0",
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
