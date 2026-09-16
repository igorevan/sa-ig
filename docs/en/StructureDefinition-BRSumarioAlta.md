# Sumário de Alta (SA) - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Resource Profile: Sumário de Alta (SA) 

 
O sumário de alta apresenta o conjunto dos principais registros realizados durante a permanência do indivíduo em um atendimento, como evolução clínica, procedimentos assistenciais, intervenções clínicas e diagnósticas, condutas adotadas e iniciadas para seguimento em clínica ou outro estabelecimento de assistência à saúde, e principalmente no final de sua permanência. A troca das informações essenciais referente ao período de permanência do indivíduo em um estabelecimento de saúde garante sua segurança na continuidade do tratamento. (Resolução CIT Nº 33, de 22 de março de 2018) 

**Usos:**

* Este Perfil não é utilizado por nenhum perfil neste guia de implementação

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/br.gov.saude.sa.fhir|current/StructureDefinition/StructureDefinition-BRSumarioAlta.json)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-BRSumarioAlta.csv), [Excel](../StructureDefinition-BRSumarioAlta.xlsx), [Schematron](../StructureDefinition-BRSumarioAlta.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "BRSumarioAlta",
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
  "url" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BRSumarioAlta",
  "version" : "1.0.0-release",
  "name" : "BRSumarioAlta",
  "title" : "Sumário de Alta (SA)",
  "status" : "active",
  "date" : "2023-12-11",
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
  "description" : "O sumário de alta apresenta o conjunto dos principais registros realizados durante a permanência do indivíduo em um atendimento, como evolução clínica, procedimentos assistenciais, intervenções clínicas e diagnósticas, condutas adotadas e iniciadas para seguimento em clínica ou outro estabelecimento de assistência à saúde, e principalmente no final de sua permanência. A troca das informações essenciais referente ao período de permanência do indivíduo em um estabelecimento de saúde garante sua segurança na continuidade do tratamento. (Resolução CIT Nº 33, de 22 de março de 2018)",
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
    "identity" : "rim",
    "uri" : "http://hl7.org/v3",
    "name" : "RIM Mapping"
  },
  {
    "identity" : "cda",
    "uri" : "http://hl7.org/v3/cda",
    "name" : "CDA (R2)"
  },
  {
    "identity" : "fhirdocumentreference",
    "uri" : "http://hl7.org/fhir/documentreference",
    "name" : "FHIR DocumentReference"
  },
  {
    "identity" : "w5",
    "uri" : "http://hl7.org/fhir/fivews",
    "name" : "FiveWs Pattern Mapping"
  }],
  "kind" : "resource",
  "abstract" : false,
  "type" : "Composition",
  "baseDefinition" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BRConjuntoMinimoDados-1.1",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Composition",
      "path" : "Composition",
      "short" : "Sumário de Alta Hospitalar",
      "definition" : "Sumário de Alta Hospitalar"
    },
    {
      "id" : "Composition.category",
      "path" : "Composition.category",
      "mapping" : [{
        "identity" : "rnds",
        "map" : "SA.2.6"
      }]
    },
    {
      "id" : "Composition.category.coding.code",
      "path" : "Composition.category.coding.code",
      "mapping" : [{
        "identity" : "rnds",
        "map" : "SA.2.6"
      }]
    },
    {
      "id" : "Composition.subject.extension:unidentifiedPatient",
      "path" : "Composition.subject.extension",
      "sliceName" : "unidentifiedPatient",
      "mapping" : [{
        "identity" : "rnds",
        "map" : "SA.1.2"
      }]
    },
    {
      "id" : "Composition.subject.identifier.value",
      "path" : "Composition.subject.identifier.value",
      "mapping" : [{
        "identity" : "rnds",
        "map" : "SA.1.1"
      }]
    },
    {
      "id" : "Composition.section",
      "path" : "Composition.section",
      "slicing" : {
        "ordered" : false,
        "rules" : "open"
      }
    },
    {
      "id" : "Composition.section:informacoesContatoAssistencial",
      "path" : "Composition.section",
      "sliceName" : "informacoesContatoAssistencial",
      "definition" : "Referencia as informações de um contato assistencial."
    },
    {
      "id" : "Composition.section:informacoesContatoAssistencial.title",
      "path" : "Composition.section.title",
      "fixedString" : "Caracterização do atendimento e Informações da alta"
    },
    {
      "id" : "Composition.section:problemasDiagnosticosAvaliados",
      "path" : "Composition.section",
      "sliceName" : "problemasDiagnosticosAvaliados",
      "definition" : "Referencia as informações de problema(s) e/ou diagnostico(s) avaliado(s), bem como lista todas as restrições funcionais e incapacidades em saúde de um paciente."
    },
    {
      "id" : "Composition.section:problemasDiagnosticosAvaliados.title",
      "path" : "Composition.section.title",
      "fixedString" : "Motivo da admissão, diagnósticos relevantes e patologias associadas"
    },
    {
      "id" : "Composition.section:procedimentosRealizados",
      "path" : "Composition.section",
      "sliceName" : "procedimentosRealizados",
      "definition" : "Referencia as informações dos procedimentos realizados."
    },
    {
      "id" : "Composition.section:procedimentosRealizados.title",
      "path" : "Composition.section.title",
      "fixedString" : "Procedimento(s) realizado(s) ou solicitado(s)"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude",
      "path" : "Composition.section",
      "sliceName" : "restricaoFuncionalIncapacidadeSaude",
      "short" : "Restrições funcionais e incapacidades em saúde",
      "definition" : "Restrições funcionais e incapacidades em saúde",
      "max" : "1"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.title",
      "path" : "Composition.section.title",
      "fixedString" : "Restrições funcionais e incapacidades em saúde"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.code",
      "path" : "Composition.section.code",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.author",
      "path" : "Composition.section.author",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.focus",
      "path" : "Composition.section.focus",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.text",
      "path" : "Composition.section.text",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.mode",
      "path" : "Composition.section.mode",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.orderedBy",
      "path" : "Composition.section.orderedBy",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.entry",
      "path" : "Composition.section.entry",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRRestricaoFuncionalIncapacidadeSaude-1.0"]
      }]
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.entry.type",
      "path" : "Composition.section.entry.type",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.entry.identifier",
      "path" : "Composition.section.entry.identifier",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.entry.display",
      "path" : "Composition.section.entry.display",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.emptyReason",
      "path" : "Composition.section.emptyReason",
      "max" : "0"
    },
    {
      "id" : "Composition.section:restricaoFuncionalIncapacidadeSaude.section",
      "path" : "Composition.section.section",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica",
      "path" : "Composition.section",
      "sliceName" : "resumoEvolucaoClinica",
      "short" : "Resumo da Evolução Clínica",
      "definition" : "Resume a evolução clínica durante a internação de um paciente, bem como referencia quaisquer informações adicionais ou complementares para a alta do paciente.",
      "min" : 1,
      "max" : "1"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.title",
      "path" : "Composition.section.title",
      "fixedString" : "Resumo da Evolução Clínica"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.code",
      "path" : "Composition.section.code",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.author",
      "path" : "Composition.section.author",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.focus",
      "path" : "Composition.section.focus",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.text",
      "path" : "Composition.section.text",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.mode",
      "path" : "Composition.section.mode",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.orderedBy",
      "path" : "Composition.section.orderedBy",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.entry",
      "path" : "Composition.section.entry",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRResumoEvolucaoClinica"]
      }]
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.entry.type",
      "path" : "Composition.section.entry.type",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.entry.identifier",
      "path" : "Composition.section.entry.identifier",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.entry.display",
      "path" : "Composition.section.entry.display",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.emptyReason",
      "path" : "Composition.section.emptyReason",
      "max" : "0"
    },
    {
      "id" : "Composition.section:resumoEvolucaoClinica.section",
      "path" : "Composition.section.section",
      "max" : "0"
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa",
      "path" : "Composition.section",
      "sliceName" : "alergiaReacaoAdversa",
      "short" : "Alergias e/ou Reações Adversas",
      "definition" : "Lista todas as alergias e/ou reações adversas do paciente durante a internação."
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.title",
      "path" : "Composition.section.title",
      "fixedString" : "Alergias e/ou reações adversas na internação"
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.code",
      "path" : "Composition.section.code",
      "max" : "0"
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.author",
      "path" : "Composition.section.author",
      "max" : "0"
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.focus",
      "path" : "Composition.section.focus",
      "max" : "0"
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.text",
      "path" : "Composition.section.text",
      "max" : "0"
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.mode",
      "path" : "Composition.section.mode",
      "max" : "0"
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.orderedBy",
      "path" : "Composition.section.orderedBy",
      "max" : "0"
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.entry",
      "path" : "Composition.section.entry",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRAlergiaReacaoAdversa-1.0"]
      }]
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.emptyReason",
      "path" : "Composition.section.emptyReason",
      "max" : "0"
    },
    {
      "id" : "Composition.section:alergiaReacaoAdversa.section",
      "path" : "Composition.section.section",
      "max" : "0"
    },
    {
      "id" : "Composition.section:prescricaoAlta",
      "path" : "Composition.section",
      "sliceName" : "prescricaoAlta",
      "short" : "Prescrição da Alta",
      "definition" : "Referencia a prescrição de medicamento realizada durante a alta do paciente.",
      "max" : "1"
    },
    {
      "id" : "Composition.section:prescricaoAlta.title",
      "path" : "Composition.section.title",
      "fixedString" : "Prescrição da Alta"
    },
    {
      "id" : "Composition.section:prescricaoAlta.code",
      "path" : "Composition.section.code",
      "max" : "0"
    },
    {
      "id" : "Composition.section:prescricaoAlta.author",
      "path" : "Composition.section.author",
      "max" : "0"
    },
    {
      "id" : "Composition.section:prescricaoAlta.focus",
      "path" : "Composition.section.focus",
      "max" : "0"
    },
    {
      "id" : "Composition.section:prescricaoAlta.text",
      "path" : "Composition.section.text",
      "max" : "0"
    },
    {
      "id" : "Composition.section:prescricaoAlta.mode",
      "path" : "Composition.section.mode",
      "max" : "0"
    },
    {
      "id" : "Composition.section:prescricaoAlta.orderedBy",
      "path" : "Composition.section.orderedBy",
      "max" : "0"
    },
    {
      "id" : "Composition.section:prescricaoAlta.entry",
      "path" : "Composition.section.entry",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRRegistroPrescricaoMedicamento"]
      }]
    },
    {
      "id" : "Composition.section:prescricaoAlta.emptyReason",
      "path" : "Composition.section.emptyReason",
      "max" : "0"
    },
    {
      "id" : "Composition.section:prescricaoAlta.section",
      "path" : "Composition.section.section",
      "max" : "0"
    },
    {
      "id" : "Composition.section:planoCuidados",
      "path" : "Composition.section",
      "sliceName" : "planoCuidados",
      "short" : "Plano de Cuidados",
      "definition" : "Referencia o plano de cuidados, instruções e recomendações na alta do paciente.",
      "max" : "1"
    },
    {
      "id" : "Composition.section:planoCuidados.title",
      "path" : "Composition.section.title",
      "fixedString" : "Plano de cuidados, instruções e recomendações (na alta)"
    },
    {
      "id" : "Composition.section:planoCuidados.code",
      "path" : "Composition.section.code",
      "max" : "0"
    },
    {
      "id" : "Composition.section:planoCuidados.author",
      "path" : "Composition.section.author",
      "max" : "0"
    },
    {
      "id" : "Composition.section:planoCuidados.focus",
      "path" : "Composition.section.focus",
      "max" : "0"
    },
    {
      "id" : "Composition.section:planoCuidados.text",
      "path" : "Composition.section.text",
      "max" : "0"
    },
    {
      "id" : "Composition.section:planoCuidados.mode",
      "path" : "Composition.section.mode",
      "max" : "0"
    },
    {
      "id" : "Composition.section:planoCuidados.orderedBy",
      "path" : "Composition.section.orderedBy",
      "max" : "0"
    },
    {
      "id" : "Composition.section:planoCuidados.entry",
      "path" : "Composition.section.entry",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRPlanoCuidados-1.0"]
      }]
    },
    {
      "id" : "Composition.section:planoCuidados.emptyReason",
      "path" : "Composition.section.emptyReason",
      "max" : "0"
    },
    {
      "id" : "Composition.section:planoCuidados.section",
      "path" : "Composition.section.section",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais",
      "path" : "Composition.section",
      "sliceName" : "informacoesAdicionais",
      "short" : "Informações Adicionais/Complementares",
      "definition" : "Este campo é destinado às informações relevantes em texto livre para a continuidade do cuidado, como resultados de exames, principais terapias medicamentosas usadas, etc, observando que este não deve ser utilizado em substituição aos blocos de informações disponíveis em outros campos do sumário de alta.",
      "max" : "1"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.title",
      "path" : "Composition.section.title",
      "fixedString" : "Informações Adicionais/Complementares"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.code",
      "path" : "Composition.section.code",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.author",
      "path" : "Composition.section.author",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.focus",
      "path" : "Composition.section.focus",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.text",
      "path" : "Composition.section.text",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.mode",
      "path" : "Composition.section.mode",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.orderedBy",
      "path" : "Composition.section.orderedBy",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.entry",
      "path" : "Composition.section.entry",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRObservacaoDescritiva-1.0"]
      }]
    },
    {
      "id" : "Composition.section:informacoesAdicionais.entry.type",
      "path" : "Composition.section.entry.type",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.entry.identifier",
      "path" : "Composition.section.entry.identifier",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.entry.display",
      "path" : "Composition.section.entry.display",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.emptyReason",
      "path" : "Composition.section.emptyReason",
      "max" : "0"
    },
    {
      "id" : "Composition.section:informacoesAdicionais.section",
      "path" : "Composition.section.section",
      "max" : "0"
    }]
  }
}

```
