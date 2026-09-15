# Imunobiológico Administrado em Rotina - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Resource Profile: Imunobiológico Administrado em Rotina 

 
Representa um imunobiológico administrado em Rotina (Portaria Conjunta SAES/SVSA/SEIDIGI Nº 25, de 27 de Novembro de 2023). 

**Usos:**

* Refere a este Perfil: [Registro de Imunobiológico Administrado na Rotina](StructureDefinition-BRRegistroImunobiologicoAdministradoRotina-2.0.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/br.gov.saude.sa.fhir|current/StructureDefinition/StructureDefinition-BRImunobiologicoAdministrado-3.0.json)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-BRImunobiologicoAdministrado-3.0.csv), [Excel](../StructureDefinition-BRImunobiologicoAdministrado-3.0.xlsx), [Schematron](../StructureDefinition-BRImunobiologicoAdministrado-3.0.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "BRImunobiologicoAdministrado-3.0",
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
  "url" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BRImunobiologicoAdministrado-3.0",
  "version" : "1.0.0-release",
  "name" : "BRImunobiologicoAdministrado",
  "title" : "Imunobiológico Administrado em Rotina",
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
  "description" : "Representa um imunobiológico administrado em Rotina (Portaria Conjunta SAES/SVSA/SEIDIGI Nº 25, de 27 de Novembro de 2023).",
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
    "identity" : "cda",
    "uri" : "http://hl7.org/v3/cda",
    "name" : "CDA (R2)"
  }],
  "kind" : "resource",
  "abstract" : false,
  "type" : "Immunization",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Immunization",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Immunization",
      "path" : "Immunization",
      "short" : "Imunobiológico Administrado",
      "definition" : "Representa o imunobiológico administrado em rotina.",
      "alias" : ["Vacinação", "Vacina Administrada"],
      "mustSupport" : true
    },
    {
      "id" : "Immunization.extension",
      "path" : "Immunization.extension",
      "min" : 2,
      "max" : "3"
    },
    {
      "id" : "Immunization.extension:grupoAtendimento",
      "path" : "Immunization.extension",
      "sliceName" : "grupoAtendimento",
      "definition" : "Identifica a classificação do grupo de atendimento dos indivíduos para a vacinação.",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "Extension",
        "profile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRGrupoAtendimento"]
      }]
    },
    {
      "id" : "Immunization.extension:condicaoMaternal",
      "path" : "Immunization.extension",
      "sliceName" : "condicaoMaternal",
      "min" : 1,
      "type" : [{
        "code" : "Extension",
        "profile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRCondicaoMaternal"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "Immunization.extension:contatoHanseniase",
      "path" : "Immunization.extension",
      "sliceName" : "contatoHanseniase",
      "definition" : "Identifica se um indivíduo possui contato próximo de pacientes que vivem com Hanseníase. Para registro do campo contato hanseníase, deverão ser utilizados as opções TRUE (T) e FALSE (F) - Verdadeiro ou Falso.\r\nRegra negocial: O campo deve ser obrigatório quando o imunobiológico for vacina Bacilo Calmette-Guérim (BCG) de code 15",
      "max" : "1",
      "type" : [{
        "code" : "Extension",
        "profile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRContatoHanseniase"]
      }]
    },
    {
      "id" : "Immunization.identifier",
      "path" : "Immunization.identifier",
      "max" : "0"
    },
    {
      "id" : "Immunization.status",
      "path" : "Immunization.status",
      "short" : "Estado da Administração do Imunobiológico",
      "fixedCode" : "completed",
      "mustSupport" : true,
      "binding" : {
        "strength" : "required",
        "description" : "Estado do Evento",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BREstadoEvento-1.0"
      }
    },
    {
      "id" : "Immunization.statusReason",
      "path" : "Immunization.statusReason",
      "max" : "0"
    },
    {
      "id" : "Immunization.vaccineCode",
      "path" : "Immunization.vaccineCode",
      "short" : "Imunobiológico",
      "definition" : "Identifica o nome do imunobiológico administrado no indivíduo.",
      "mustSupport" : true,
      "binding" : {
        "strength" : "required",
        "description" : "Imunobiológico",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BRImunobiologico-1.0"
      }
    },
    {
      "id" : "Immunization.vaccineCode.coding",
      "path" : "Immunization.vaccineCode.coding",
      "min" : 1,
      "max" : "1"
    },
    {
      "id" : "Immunization.vaccineCode.coding.system",
      "path" : "Immunization.vaccineCode.coding.system",
      "min" : 1
    },
    {
      "id" : "Immunization.vaccineCode.coding.code",
      "path" : "Immunization.vaccineCode.coding.code",
      "min" : 1
    },
    {
      "id" : "Immunization.vaccineCode.coding.display",
      "path" : "Immunization.vaccineCode.coding.display",
      "max" : "0"
    },
    {
      "id" : "Immunization.vaccineCode.coding.userSelected",
      "path" : "Immunization.vaccineCode.coding.userSelected",
      "max" : "0"
    },
    {
      "id" : "Immunization.vaccineCode.text",
      "path" : "Immunization.vaccineCode.text",
      "max" : "0"
    },
    {
      "id" : "Immunization.patient",
      "path" : "Immunization.patient",
      "short" : "Indivíduo",
      "definition" : "Indivíduo que recebeu o imunobiológico.",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRIndividuo-1.0"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "Immunization.patient.identifier.use",
      "path" : "Immunization.patient.identifier.use",
      "max" : "0"
    },
    {
      "id" : "Immunization.patient.identifier.type",
      "path" : "Immunization.patient.identifier.type",
      "max" : "0"
    },
    {
      "id" : "Immunization.patient.identifier.system",
      "path" : "Immunization.patient.identifier.system",
      "min" : 1
    },
    {
      "id" : "Immunization.patient.identifier.value",
      "path" : "Immunization.patient.identifier.value",
      "min" : 1
    },
    {
      "id" : "Immunization.patient.identifier.period",
      "path" : "Immunization.patient.identifier.period",
      "max" : "0"
    },
    {
      "id" : "Immunization.patient.identifier.assigner",
      "path" : "Immunization.patient.identifier.assigner",
      "max" : "0"
    },
    {
      "id" : "Immunization.patient.display",
      "path" : "Immunization.patient.display",
      "max" : "0"
    },
    {
      "id" : "Immunization.encounter",
      "path" : "Immunization.encounter",
      "max" : "0"
    },
    {
      "id" : "Immunization.occurrence[x]",
      "path" : "Immunization.occurrence[x]",
      "short" : "Data da Administração do Imunobiológico",
      "definition" : "Data em que o imunobiológico foi administrado. O padrão da data deve seguir a ISO8601.\nRegra negocial: A data não pode ser maior que o dia vigente.",
      "type" : [{
        "code" : "dateTime"
      }],
      "mustSupport" : true
    },
    {
      "id" : "Immunization.recorded",
      "path" : "Immunization.recorded",
      "max" : "0"
    },
    {
      "id" : "Immunization.primarySource",
      "path" : "Immunization.primarySource",
      "short" : "Indicação da fonte do registro",
      "definition" : "Indica se o registro é de fonte própria (true) ou se é derivado de uma fonte externa (false)."
    },
    {
      "id" : "Immunization.reportOrigin",
      "path" : "Immunization.reportOrigin",
      "short" : "Registro de Origem",
      "definition" : "Referencia a origem deste registro de fonte externa.",
      "binding" : {
        "strength" : "required",
        "description" : "Registro de Origem",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BRRegistroOrigem"
      }
    },
    {
      "id" : "Immunization.location",
      "path" : "Immunization.location",
      "short" : "Indicação do país de origem do registro da vacina",
      "definition" : "Identifica se o registro da administração da vacina, realizado por transcrição de caderneta, foi realizado no Brasil ou em outro País."
    },
    {
      "id" : "Immunization.location.reference",
      "path" : "Immunization.location.reference",
      "max" : "0"
    },
    {
      "id" : "Immunization.location.type",
      "path" : "Immunization.location.type",
      "max" : "0"
    },
    {
      "id" : "Immunization.location.identifier",
      "path" : "Immunization.location.identifier",
      "min" : 1
    },
    {
      "id" : "Immunization.location.identifier.use",
      "path" : "Immunization.location.identifier.use",
      "max" : "0"
    },
    {
      "id" : "Immunization.location.identifier.type",
      "path" : "Immunization.location.identifier.type",
      "max" : "0"
    },
    {
      "id" : "Immunization.location.identifier.system",
      "path" : "Immunization.location.identifier.system",
      "short" : "País de origem do registro da vacina",
      "min" : 1,
      "fixedUri" : "http://www.saude.gov.br/fhir/r4/CodeSystem/BRPais"
    },
    {
      "id" : "Immunization.location.identifier.value",
      "path" : "Immunization.location.identifier.value",
      "short" : "País de origem do registro da vacina",
      "min" : 1,
      "binding" : {
        "strength" : "required",
        "description" : "Códigos para representação de países",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BRPais-1.0"
      }
    },
    {
      "id" : "Immunization.location.identifier.period",
      "path" : "Immunization.location.identifier.period",
      "max" : "0"
    },
    {
      "id" : "Immunization.location.identifier.assigner",
      "path" : "Immunization.location.identifier.assigner",
      "max" : "0"
    },
    {
      "id" : "Immunization.location.display",
      "path" : "Immunization.location.display",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer",
      "path" : "Immunization.manufacturer",
      "short" : "Fabricante",
      "definition" : "Identifica o laboratório fabricante do imunobiológico administrado no indivíduo.\nRegra negocial: Para registro de transcrição de caderneta de vacinação, este campo é opcional.",
      "mustSupport" : true
    },
    {
      "id" : "Immunization.manufacturer.reference",
      "path" : "Immunization.manufacturer.reference",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.type",
      "path" : "Immunization.manufacturer.type",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier",
      "path" : "Immunization.manufacturer.identifier",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "Immunization.manufacturer.identifier.use",
      "path" : "Immunization.manufacturer.identifier.use",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.type",
      "path" : "Immunization.manufacturer.identifier.type",
      "max" : "0",
      "mustSupport" : false
    },
    {
      "id" : "Immunization.manufacturer.identifier.type.coding",
      "path" : "Immunization.manufacturer.identifier.type.coding",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.type.coding.id",
      "path" : "Immunization.manufacturer.identifier.type.coding.id",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.type.coding.system",
      "path" : "Immunization.manufacturer.identifier.type.coding.system",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.type.coding.version",
      "path" : "Immunization.manufacturer.identifier.type.coding.version",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.type.coding.code",
      "path" : "Immunization.manufacturer.identifier.type.coding.code",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.type.coding.display",
      "path" : "Immunization.manufacturer.identifier.type.coding.display",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.type.coding.userSelected",
      "path" : "Immunization.manufacturer.identifier.type.coding.userSelected",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.type.text",
      "path" : "Immunization.manufacturer.identifier.type.text",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.system",
      "path" : "Immunization.manufacturer.identifier.system",
      "short" : "Fabricante PNI",
      "definition" : "URL que define o system BRFabricantePNI como referência para esse elemento.",
      "min" : 1,
      "fixedUri" : "http://www.saude.gov.br/fhir/r4/CodeSystem/BRFabricantePNI",
      "mustSupport" : true
    },
    {
      "id" : "Immunization.manufacturer.identifier.value",
      "path" : "Immunization.manufacturer.identifier.value",
      "short" : "Fabricante do imunobiológico.",
      "min" : 1,
      "mustSupport" : true,
      "binding" : {
        "strength" : "required",
        "description" : "O código do fabricante do imunobiológico.",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BRFabricanteImunobiologico-1.0"
      }
    },
    {
      "id" : "Immunization.manufacturer.identifier.period",
      "path" : "Immunization.manufacturer.identifier.period",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.identifier.assigner",
      "path" : "Immunization.manufacturer.identifier.assigner",
      "max" : "0"
    },
    {
      "id" : "Immunization.manufacturer.display",
      "path" : "Immunization.manufacturer.display",
      "short" : "Nome do fabricante",
      "max" : "0"
    },
    {
      "id" : "Immunization.lotNumber",
      "path" : "Immunization.lotNumber",
      "short" : "Lote",
      "definition" : "Identifica o lote do imunobiológico de acordo com o fabricante.\r\nO lote é fundamental para identificação de características do imunobiológico. É uma informação presente na embalagem do produto ou, algumas vezes, na caderneta de vacinação.\nRegra negocial: Para registro de transcrição de caderneta de vacinação, este campo é opcional.",
      "mustSupport" : true
    },
    {
      "id" : "Immunization.expirationDate",
      "path" : "Immunization.expirationDate",
      "short" : "Data de expiração do imunobiológico",
      "definition" : "Data de expiração do imunobiológico"
    },
    {
      "id" : "Immunization.site",
      "path" : "Immunization.site",
      "short" : "Local de Aplicação",
      "definition" : "Identifica a localização anatômica em que o imunobiológico foi aplicado.",
      "min" : 1,
      "mustSupport" : true,
      "binding" : {
        "strength" : "required",
        "description" : "Local de Aplicação",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BRLocalAplicacao-1.0"
      }
    },
    {
      "id" : "Immunization.site.coding",
      "path" : "Immunization.site.coding",
      "min" : 1,
      "max" : "1"
    },
    {
      "id" : "Immunization.site.coding.system",
      "path" : "Immunization.site.coding.system",
      "min" : 1
    },
    {
      "id" : "Immunization.site.coding.code",
      "path" : "Immunization.site.coding.code",
      "min" : 1
    },
    {
      "id" : "Immunization.site.coding.display",
      "path" : "Immunization.site.coding.display",
      "max" : "0"
    },
    {
      "id" : "Immunization.site.coding.userSelected",
      "path" : "Immunization.site.coding.userSelected",
      "max" : "0"
    },
    {
      "id" : "Immunization.site.text",
      "path" : "Immunization.site.text",
      "max" : "0"
    },
    {
      "id" : "Immunization.route",
      "path" : "Immunization.route",
      "short" : "Via de Administração",
      "definition" : "Identifica a via com que o imunobiológico administrado entra em contato com o organismo.",
      "min" : 1,
      "mustSupport" : true,
      "binding" : {
        "strength" : "required",
        "description" : "Via de Administração",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BRViaAdministracao-1.0"
      }
    },
    {
      "id" : "Immunization.route.coding",
      "path" : "Immunization.route.coding",
      "min" : 1,
      "max" : "1"
    },
    {
      "id" : "Immunization.route.coding.system",
      "path" : "Immunization.route.coding.system",
      "min" : 1
    },
    {
      "id" : "Immunization.route.coding.code",
      "path" : "Immunization.route.coding.code",
      "min" : 1
    },
    {
      "id" : "Immunization.route.coding.display",
      "path" : "Immunization.route.coding.display",
      "max" : "0"
    },
    {
      "id" : "Immunization.route.coding.userSelected",
      "path" : "Immunization.route.coding.userSelected",
      "max" : "0"
    },
    {
      "id" : "Immunization.route.text",
      "path" : "Immunization.route.text",
      "max" : "0"
    },
    {
      "id" : "Immunization.doseQuantity",
      "path" : "Immunization.doseQuantity",
      "max" : "0"
    },
    {
      "id" : "Immunization.performer",
      "path" : "Immunization.performer",
      "short" : "Profissional Executante",
      "definition" : "Informações sobre o profissional que administrou o imunobiológico.",
      "min" : 1,
      "max" : "1",
      "mustSupport" : true
    },
    {
      "id" : "Immunization.performer.function",
      "path" : "Immunization.performer.function",
      "short" : "Especialidade do profissional prescritor",
      "definition" : "Identifica a especialidade do profissional que prescreveu a administração do imunobiológico por meio do Código Brasileiro de Ocupações (CBO). Regra negocial: Quando a estratégia de vacinação for Especial, o campo deve ser obrigatório.",
      "min" : 0,
      "max" : "1",
      "binding" : {
        "strength" : "required",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BROcupacao-1.0"
      }
    },
    {
      "id" : "Immunization.performer.function.coding",
      "path" : "Immunization.performer.function.coding",
      "min" : 1,
      "max" : "1"
    },
    {
      "id" : "Immunization.performer.function.coding.system",
      "path" : "Immunization.performer.function.coding.system",
      "min" : 1
    },
    {
      "id" : "Immunization.performer.function.coding.code",
      "path" : "Immunization.performer.function.coding.code",
      "min" : 1
    },
    {
      "id" : "Immunization.performer.function.coding.display",
      "path" : "Immunization.performer.function.coding.display",
      "max" : "0"
    },
    {
      "id" : "Immunization.performer.function.coding.userSelected",
      "path" : "Immunization.performer.function.coding.userSelected",
      "max" : "0"
    },
    {
      "id" : "Immunization.performer.function.text",
      "path" : "Immunization.performer.function.text",
      "max" : "0"
    },
    {
      "id" : "Immunization.performer.actor",
      "path" : "Immunization.performer.actor",
      "short" : "Identificador do profissional",
      "definition" : "Identifica o número do Cadastro Nacional de Saúde (CNS) do profissional de saúde que realizou o atendimento ou transcrição. Deverá ser utilizado para a identificação, o Cartão Nacional de Saúde (CNS) do profissional.",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRProfissional-1.0"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "Immunization.performer.actor.reference",
      "path" : "Immunization.performer.actor.reference",
      "min" : 1
    },
    {
      "id" : "Immunization.performer.actor.type",
      "path" : "Immunization.performer.actor.type",
      "max" : "0"
    },
    {
      "id" : "Immunization.performer.actor.identifier",
      "path" : "Immunization.performer.actor.identifier",
      "max" : "0"
    },
    {
      "id" : "Immunization.performer.actor.display",
      "path" : "Immunization.performer.actor.display",
      "max" : "0"
    },
    {
      "id" : "Immunization.note",
      "path" : "Immunization.note",
      "max" : "0"
    },
    {
      "id" : "Immunization.reasonCode",
      "path" : "Immunization.reasonCode",
      "max" : "0"
    },
    {
      "id" : "Immunization.reasonReference",
      "path" : "Immunization.reasonReference",
      "short" : "Motivo de Indicação",
      "definition" : "Identifica o código da Classificação Internacional de Doenças (CID) do motivo da indicação para administração do imunobiológico.\n\nRegra negocial: Quando a estratégia de vacinação for \"Especial\", o campo deve ser obrigatório.",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BRCID10Avaliado-1.0"]
      }]
    },
    {
      "id" : "Immunization.isSubpotent",
      "path" : "Immunization.isSubpotent",
      "max" : "0"
    },
    {
      "id" : "Immunization.subpotentReason",
      "path" : "Immunization.subpotentReason",
      "max" : "0"
    },
    {
      "id" : "Immunization.education",
      "path" : "Immunization.education",
      "max" : "0"
    },
    {
      "id" : "Immunization.programEligibility",
      "path" : "Immunization.programEligibility",
      "max" : "0"
    },
    {
      "id" : "Immunization.fundingSource",
      "path" : "Immunization.fundingSource",
      "max" : "0"
    },
    {
      "id" : "Immunization.reaction",
      "path" : "Immunization.reaction",
      "max" : "0"
    },
    {
      "id" : "Immunization.protocolApplied",
      "path" : "Immunization.protocolApplied",
      "min" : 1,
      "max" : "1",
      "mustSupport" : true
    },
    {
      "id" : "Immunization.protocolApplied.extension",
      "path" : "Immunization.protocolApplied.extension",
      "min" : 1,
      "max" : "2"
    },
    {
      "id" : "Immunization.protocolApplied.extension:strategy",
      "path" : "Immunization.protocolApplied.extension",
      "sliceName" : "strategy",
      "definition" : "Identifica a estratégia de vacinação adotada, conforme estabelecidos pelo Programa Nacional de Imunização (PNI) e disponibilizado nos CodeSystems da Rede Nacional de Dados em Saúde (RNDS).",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "Extension",
        "profile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BREstrategiaVacinacao-1.0"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "Immunization.protocolApplied.extension:pesquisaClinica",
      "path" : "Immunization.protocolApplied.extension",
      "sliceName" : "pesquisaClinica",
      "short" : "Pesquisa Clínica",
      "definition" : "Dados do Estudo Clínico para o desenvolvimento do imunobiológico administrado.",
      "max" : "1",
      "type" : [{
        "code" : "Extension",
        "profile" : ["http://www.saude.gov.br/fhir/r4/StructureDefinition/BREstrategiaVacinacaoPesquisa-1.0"]
      }]
    },
    {
      "id" : "Immunization.protocolApplied.extension:pesquisaClinica.extension",
      "path" : "Immunization.protocolApplied.extension.extension",
      "max" : "3"
    },
    {
      "id" : "Immunization.protocolApplied.extension:pesquisaClinica.extension:numeroProtocoloEstudoANVISA",
      "path" : "Immunization.protocolApplied.extension.extension",
      "sliceName" : "numeroProtocoloEstudoANVISA",
      "short" : "ANVISA Protocolo Estudo",
      "definition" : "Número do protocolo do estudo clínico na ANVISA: identifica o número do protocolo do estudo clínico autorizado pela Agência Nacional de Vigilância Sanitária para administração de vacinas."
    },
    {
      "id" : "Immunization.protocolApplied.extension:pesquisaClinica.extension:numeroVersaoProtocoloEstudo",
      "path" : "Immunization.protocolApplied.extension.extension",
      "sliceName" : "numeroVersaoProtocoloEstudo",
      "short" : "ANVISA Protocolo Versão",
      "definition" : "Número da versão do protocolo do estudo na ANVISA: identifica o número da versão do protocolo do estudo clínico autorizado pela Agência Nacional de Vigilância Sanitária para administração de vacinas."
    },
    {
      "id" : "Immunization.protocolApplied.extension:pesquisaClinica.extension:numeroRegistroVacinaAnvisa",
      "path" : "Immunization.protocolApplied.extension.extension",
      "sliceName" : "numeroRegistroVacinaAnvisa",
      "short" : "ANVISA Num Registro",
      "definition" : "Número do registro sanitário da vacina na ANVISA. Este registro pode ser emergencial ou definitivo.\r\nIdentifica o número do registro sanitário da vacina registrado na Agência Nacional de Vigilância Sanitária."
    },
    {
      "id" : "Immunization.protocolApplied.series",
      "path" : "Immunization.protocolApplied.series",
      "max" : "0"
    },
    {
      "id" : "Immunization.protocolApplied.authority",
      "path" : "Immunization.protocolApplied.authority",
      "max" : "0"
    },
    {
      "id" : "Immunization.protocolApplied.targetDisease",
      "path" : "Immunization.protocolApplied.targetDisease",
      "max" : "0"
    },
    {
      "id" : "Immunization.protocolApplied.doseNumber[x]",
      "path" : "Immunization.protocolApplied.doseNumber[x]",
      "short" : "Dose",
      "definition" : "Identifica o registro da dose da vacina administrada no indivíduo.",
      "type" : [{
        "code" : "string"
      }],
      "mustSupport" : true,
      "binding" : {
        "strength" : "required",
        "description" : "Dose do Imunobiológico",
        "valueSet" : "http://www.saude.gov.br/fhir/r4/ValueSet/BRDose-1.0"
      }
    },
    {
      "id" : "Immunization.protocolApplied.seriesDoses[x]",
      "path" : "Immunization.protocolApplied.seriesDoses[x]",
      "max" : "0"
    }]
  }
}

```
