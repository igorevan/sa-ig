# Grupo de Atendimento (CodeSystem) - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## CodeSystem: Grupo de Atendimento (CodeSystem) 

 
Domínio que identifica o tipo de grupo de atendimento que o indivíduo apresentou para a vacinação em campanha. 

This Code system is referenced in the definition of the following value sets:

* [Tipo de grupo de atendimento (ValueSet)](ValueSet-BRGrupoAtendimento-1.0.md)

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "BRGrupoAtendimento",
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
  "url" : "http://www.saude.gov.br/fhir/r4/CodeSystem/BRGrupoAtendimento",
  "version" : "1.0.0-release",
  "name" : "BRGrupoAtendimento",
  "title" : "Grupo de Atendimento (CodeSystem)",
  "status" : "active",
  "experimental" : false,
  "date" : "2021-08-20T14:59:27.326+00:00",
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
  "description" : "Domínio que identifica o tipo de grupo de atendimento que o indivíduo apresentou para a vacinação em campanha.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "BR"
    }]
  }],
  "caseSensitive" : true,
  "content" : "complete",
  "property" : [{
    "code" : "Category",
    "description" : "Identifica a classificação macro do grupo de atendimento para a vacinação, agregando descrições específicas de indivíduos que compartilham características clínicas, epidemiológicas, ocupacionais, etárias ou sociais comuns, com o objetivo de padronizar registros, apoiar estratégias de imunização e viabilizar análises agregadas nos sistemas de informação em saúde.",
    "type" : "string"
  },
  {
    "code" : "inactive",
    "uri" : "http://hl7.org/fhir/concept-properties#inactive",
    "description" : "Status do Grupo de Atendimento em que determina se ele está apto para uso no registro de doses aplicadas. Serão aceitos códigos inativos apenas em caso de Transcrição de Caderneta.",
    "type" : "boolean"
  }],
  "concept" : [{
    "code" : "00",
    "display" : "Sem registro no modelo de informação de origem"
  },
  {
    "code" : "000101",
    "display" : "Hemoglobinopatia grave",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000102",
    "display" : "Neoplasias",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000103",
    "display" : "Diabetes Mellitus",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000104",
    "display" : "Pneumopatias Crônicas Graves",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000105",
    "display" : "Doença Renal Crônica",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000106",
    "display" : "Doenças Cardiovasculares e Cerebrovasculares",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000107",
    "display" : "Hipertensão de difícil controle ou com complicações/lesão de órgão alvo",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000108",
    "display" : "Indivíduos Transplantados de Órgão Sólido",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000109",
    "display" : "Obesidade Grave (Imc≥40)",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000110",
    "display" : "Síndrome de Down",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000111",
    "display" : "Outros Imunocomprometidos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000112",
    "display" : "Indivíduos Transplantados de Medula Óssea",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000114",
    "display" : "Cirrose hepática",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000115",
    "display" : "Doença neurológica crônica",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000116",
    "display" : "Doença cardiovascular",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000117",
    "display" : "Imunocomprometidos",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000118",
    "display" : "Trissomias",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000119",
    "display" : "Doença Hepática Crônica",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000120",
    "display" : "Prematuridade",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000121",
    "display" : "Anomalias de vias aéreas",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000122",
    "display" : "Obesidade (score-Z acima de +2)",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000123",
    "display" : "Erros Inatos da Imunidade (EII)",
    "property" : [{
      "code" : "Category",
      "valueString" : "Comorbidades"
    }]
  },
  {
    "code" : "000201",
    "display" : "Pessoas de 18 a 64 anos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000202",
    "display" : "Pessoas de 65 a 69 anos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000203",
    "display" : "Pessoas de 70 a 74 anos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000204",
    "display" : "Pessoas de 75 a 79 anos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000205",
    "display" : "Pessoas de 80 anos ou mais",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000206",
    "display" : "Pessoas de 12 a 17 anos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000207",
    "display" : "Pessoas de 5 a 11 anos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000208",
    "display" : "Pessoas de 3 a 4 anos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000209",
    "display" : "Pessoas de 6 meses a 2 anos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000210",
    "display" : "Faixa Etária",
    "property" : [{
      "code" : "Category",
      "valueString" : "Faixa Etária"
    }]
  },
  {
    "code" : "000301",
    "display" : "Pessoas de 60 nos ou mais Institucionalizadas",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Pessoas Institucionalizadas"
    }]
  },
  {
    "code" : "000302",
    "display" : "Pessoas Institucionalizadas",
    "property" : [{
      "code" : "Category",
      "valueString" : "Pessoas Institucionalizadas"
    }]
  },
  {
    "code" : "000401",
    "display" : "Marinha do Brasil - MB",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças Armadas (membros ativos)"
    }]
  },
  {
    "code" : "000402",
    "display" : "Exército Brasileiro - EB",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças Armadas (membros ativos)"
    }]
  },
  {
    "code" : "000403",
    "display" : "Força Aérea Brasileira - FAB",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças Armadas (membros ativos)"
    }]
  },
  {
    "code" : "000501",
    "display" : "Bombeiro Civil",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças de Segurança e Salvamento"
    }]
  },
  {
    "code" : "000502",
    "display" : "Bombeiro Militar",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças de Segurança e Salvamento"
    }]
  },
  {
    "code" : "000503",
    "display" : "Guarda Municipal",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças de Segurança e Salvamento"
    }]
  },
  {
    "code" : "000504",
    "display" : "Policial Rodoviário Federal",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças de Segurança e Salvamento"
    }]
  },
  {
    "code" : "000505",
    "display" : "Policial Civil",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças de Segurança e Salvamento"
    }]
  },
  {
    "code" : "000506",
    "display" : "Policial Federal",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças de Segurança e Salvamento"
    }]
  },
  {
    "code" : "000507",
    "display" : "Policial Militar",
    "property" : [{
      "code" : "Category",
      "valueString" : "Forças de Segurança e Salvamento"
    }]
  },
  {
    "code" : "000601",
    "display" : "Quilombola",
    "property" : [{
      "code" : "Category",
      "valueString" : "Povos e Comunidades Tradicionais"
    }]
  },
  {
    "code" : "000602",
    "display" : "Ribeirinha",
    "property" : [{
      "code" : "Category",
      "valueString" : "Povos e Comunidades Tradicionais"
    }]
  },
  {
    "code" : "000603",
    "display" : "Crianças Quilombolas",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Povos e Comunidades Tradicionais"
    }]
  },
  {
    "code" : "000604",
    "display" : "Crianças Ribeirinhas",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Povos e Comunidades Tradicionais"
    }]
  },
  {
    "code" : "000701",
    "display" : "Povos indígenas em terras indígenas",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Povos Indígenas"
    }]
  },
  {
    "code" : "000702",
    "display" : "Crianças Indígenas",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Povos Indígenas"
    }]
  },
  {
    "code" : "000703",
    "display" : "Povos indígenas vivendo em terras indígenas",
    "property" : [{
      "code" : "Category",
      "valueString" : "Povos Indígenas"
    }]
  },
  {
    "code" : "000704",
    "display" : "Povos indígenas vivendo fora das terras indígenas",
    "property" : [{
      "code" : "Category",
      "valueString" : "Povos Indígenas"
    }]
  },
  {
    "code" : "000801",
    "display" : "Ensino Básico",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores da Educação"
    }]
  },
  {
    "code" : "000802",
    "display" : "Ensino Superior",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores da Educação"
    }]
  },
  {
    "code" : "000901",
    "display" : "Auxiliar de Veterinário",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000902",
    "display" : "Biólogo",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000903",
    "display" : "Biomédico",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000904",
    "display" : "Cozinheiro e Auxiliares",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000905",
    "display" : "Cuidador de Idosos",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000906",
    "display" : "Doula/Parteira",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000907",
    "display" : "Enfermeiro(a)",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000908",
    "display" : "Farmacêutico",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000909",
    "display" : "Fisioterapeutas",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000910",
    "display" : "Fonoaudiólogo",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000911",
    "display" : "Funcionário do Sistema Funerário que tenham contato com cadáveres potencialmente contaminados",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000912",
    "display" : "Médico",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000913",
    "display" : "Médico Veterinário",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000914",
    "display" : "Motorista de Ambulância",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000915",
    "display" : "Nutricionista",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000916",
    "display" : "Odontologista",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000917",
    "display" : "Profissionais e Auxiliares de limpeza",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000918",
    "display" : "Profissionais de Educação Física",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000919",
    "display" : "Psicólogo",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000920",
    "display" : "Recepcionista",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000921",
    "display" : "Segurança",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000922",
    "display" : "Assistente Social",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000923",
    "display" : "Técnico de Enfermagem",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000924",
    "display" : "Técnico de Veterinário",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000925",
    "display" : "Terapeuta Ocupacional",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000926",
    "display" : "Outros Trabalhadores da Saúde",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000927",
    "display" : "Auxiliar de Enfermagem",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000928",
    "display" : "Técnico de Odontologia",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000929",
    "display" : "Acadêmicos/estudantes em estágio em estabelecimentos de saúde",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000930",
    "display" : "Agente de Combate a Endemias - ACE",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000931",
    "display" : "Agente Comunitário de Saúde - ACS",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000932",
    "display" : "Auxiliar em Saúde Bucal - ASB",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "000933",
    "display" : "Técnico em Saúde Bucal - TSB",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Saúde"
    }]
  },
  {
    "code" : "001001",
    "display" : "Aéreo",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Transporte"
    }]
  },
  {
    "code" : "001002",
    "display" : "Caminhoneiro",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Transporte"
    }]
  },
  {
    "code" : "001003",
    "display" : "Coletivo Rodoviário Passageiros Urbano e de Longo Curso",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Transporte"
    }]
  },
  {
    "code" : "001004",
    "display" : "Ferroviário",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Transporte"
    }]
  },
  {
    "code" : "001005",
    "display" : "Metroviário",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Transporte"
    }]
  },
  {
    "code" : "001006",
    "display" : "Aquaviário",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Transporte"
    }]
  },
  {
    "code" : "001101",
    "display" : "Pessoas com Deficiência Institucionalizadas",
    "property" : [{
      "code" : "Category",
      "valueString" : "Pessoas com Deficiência"
    }]
  },
  {
    "code" : "001102",
    "display" : "Pessoas com Deficiência Permanente",
    "property" : [{
      "code" : "Category",
      "valueString" : "Pessoas com Deficiência"
    }]
  },
  {
    "code" : "001201",
    "display" : "Pessoas em Situação de Rua",
    "property" : [{
      "code" : "Category",
      "valueString" : "Pessoas em Situação de Rua"
    }]
  },
  {
    "code" : "001301",
    "display" : "Trabalhadores Portuários",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores Portuários"
    }]
  },
  {
    "code" : "001401",
    "display" : "Funcionário do Sistema de Privação de Liberdade",
    "property" : [{
      "code" : "Category",
      "valueString" : "Funcionário do Sistema de Privação de Liberdade"
    }]
  },
  {
    "code" : "001501",
    "display" : "População Privada de Liberdade",
    "property" : [{
      "code" : "Category",
      "valueString" : "População Privada de Liberdade"
    }]
  },
  {
    "code" : "001502",
    "display" : "Adolescentes cumprindo medidas Socioeducativas",
    "property" : [{
      "code" : "Category",
      "valueString" : "População Privada de Liberdade"
    }]
  },
  {
    "code" : "001601",
    "display" : "Trabalhadores Industriais",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores Industriais"
    }]
  },
  {
    "code" : "001701",
    "display" : "Trabalhadores de limpeza urbana e manejo de resíduos sólidos",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Limpeza Urbana"
    }]
  },
  {
    "code" : "001801",
    "display" : "Gestante",
    "property" : [{
      "code" : "Category",
      "valueString" : "Gestante"
    }]
  },
  {
    "code" : "001901",
    "display" : "Puérpera",
    "property" : [{
      "code" : "Category",
      "valueString" : "Puérpera"
    }]
  },
  {
    "code" : "002001",
    "display" : "População Rural",
    "property" : [{
      "code" : "Category",
      "valueString" : "População Rural"
    }]
  },
  {
    "code" : "002101",
    "display" : "Profissionais dos Correios",
    "property" : [{
      "code" : "Category",
      "valueString" : "Trabalhadores de Logística"
    }]
  },
  {
    "code" : "002201",
    "display" : "Pessoas com Transtorno do Espectro Autista (TEA)",
    "property" : [{
      "code" : "Category",
      "valueString" : "Transtorno do Desenvolvimento"
    }]
  },
  {
    "code" : "999999",
    "display" : "Outros Grupos",
    "property" : [{
      "code" : "inactive",
      "valueBoolean" : true
    },
    {
      "code" : "Category",
      "valueString" : "Outros"
    }]
  }]
}

```
